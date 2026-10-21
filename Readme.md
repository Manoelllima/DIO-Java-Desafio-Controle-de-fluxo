# Controle de fluxo — desafio

Este desafio faz parte da trilha de Java básico da [DIO](https://www.dio.me/) e aborda o conteúdo do módulo **Controle de fluxo**.

**Instrutor:** Gleyson Sampaio

## Enunciado

Crie o projeto `DesafioControleFluxo` com as classes `Contador.java` e `ParametrosInvalidosException.java`.

O programa deve receber dois números inteiros pelo terminal. O primeiro número não pode ser maior que o segundo. A diferença entre eles determina a quantidade de iterações de um laço `for`, que deve imprimir cada número de 1 até essa quantidade no console.

Por exemplo, para as entradas `12` e `30`, a diferença é `18`; portanto, o programa deve imprimir:

```text
Imprimindo o número 1
Imprimindo o número 2
...
Imprimindo o número 18
```

Se o primeiro parâmetro for maior que o segundo, lance a exceção personalizada `ParametrosInvalidosException` com a mensagem:

```text
O segundo parâmetro deve ser maior que o primeiro
```

## Código inicial

Complete os trechos indicados por `??` e implemente a validação e o laço de contagem:

```java
public class Contador {
    public static void main(String[] args) {
        Scanner terminal = new Scanner(System.in);
        System.out.println("Digite o primeiro parâmetro");
        int parametroUm = terminal.??;
        System.out.println("Digite o segundo parâmetro");
        int parametroDois = terminal.??;

        try {
            // Chama o método que contém a lógica de contagem.
            contar(parametroUm, parametroDois);
        } catch (?? exception) {
            // Imprima a mensagem definida no enunciado.
        }
    }

    static void contar(int parametroUm, int parametroDois)
            throws ParametrosInvalidosException {
        // Valide os parâmetros e lance a exceção, se necessário.

        int contagem = parametroDois - parametroUm;
        // Imprima os números de 1 até contagem.
    }
}
```

## Estrutura

- `DesafioControleFluxo/Contador.java`: lê os parâmetros, valida a ordem e executa a contagem.
- `DesafioControleFluxo/ParametrosInvalidosException.java`: define a exceção para parâmetros inválidos.

## Como executar

Na pasta `ControleDeFluxo`, compile os arquivos:

```bash
javac DesafioControleFluxo\*.java
```

Em seguida, execute o programa:

```bash
java DesafioControleFluxo.Contador
```
