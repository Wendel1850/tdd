*Exemplo de Código para Teste TDD*

Aqui está um exemplo de código em Java com JUnit para testar a funcionalidade de soma de dois números utilizando TDD:
import org.junit.Test;
import static org.junit.Assert.assertEquals;

public class CalculadoraTest {
    @Test
    public void testSomaDoisNumeros() {
        // Arrange
        Calculadora calculadora = new Calculadora();
        int num1 = 2;
        int num2 = 3;

        // Act
        int resultado = calculadora.soma(num1, num2);

        // Assert
        assertEquals(5, resultado);
    }
}

public class Calculadora {
    // Inicialmente, a classe Calculadora está vazia
}
*Executando o teste:*

Quando executamos o teste, ele falha porque a classe Calculadora não tem o método soma.

*Implementando a lógica:*

Para fazer o teste passar, implementamos a lógica de soma na classe Calculadora:
public class Calculadora {
    public int soma(int num1, int num2) {
        return num1 + num2;
    }
}
*Executando o teste novamente:*

Quando executamos o teste novamente, ele passa porque a lógica de soma está implementada corretamente.

*Refatorando:*

Não há necessidade de refatorar o código nesse exemplo, pois ele é simples e fácil de entender.

*Adicionando mais testes:*

Podemos adicionar mais testes para garantir que a funcionalidade de soma esteja funcionando corretamente para diferentes casos:
@Test
public void testSomaDoisNumerosNegativos() {
    Calculadora calculadora = new Calculadora();
    int num1 = -2;
    int num2 = -3;
    int resultado = calculadora.soma(num1, num2);
    assertEquals(-5, resultado);
}

@Test
public void testSomaUmNumeroPositivoEUmNegativo() {
    Calculadora calculadora = new Calculadora();
    int num1 = 2;
    int num2 = -3;
    int resultado = calculadora.soma(num1, num2);
    assertEquals(-1, resultado);
}
Esse exemplo de código demonstra como utilizar TDD para desenvolver a funcionalidade de soma de dois números de forma incremental e segura.
