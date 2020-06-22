# Revisão UML - Diagrama de classes

![Exemplo de diagrama de classes](/static/image01.jpeg)

*Exemplo de diagrama de classes.*

Este é um **diagrama de classes**, componente bem comum do UML. O modelo base, à esquerda, descreve sua composição. Os `atributos` são as características e estados da classe, enquanto os `metodos` referem-se as funcionalidades que uma classe pode ter. À direita temos um exemplo com o tema futebol, com a classe simbolizando o jogador.

## Associação entre classes

Os diagramas de classes podem interagir entre si criando **associações**. Tal propriedade pode ser do tipo:

- Unária: Quando referencia-se a própria classe.

- Binária: Quando uma classe referencia outra classe.

- Múltipla (n-ária): Podem ser identificadas quando uma classe se conecta a outra por meio de uma classe intermediária.

A imagem abaixo apresenta um rascunho exemplificando cada tipo de associação:

![Exemplo de associações](/static/image02.jpeg)

*Exemplo de tipos de associação em diagrama de classes.*

## Cardinalidade

Determina quantos objetos no sistema são possíveis em cada vértice da associação.

## Navegação

Valida se é possível o acesso a outro objeto da mesma associação.

## Herança

Neste conceito uma classe deriva de outra classe (chamada de superclasse), abstraindo todas as características base e podendo adicionar ou moldar novas características, assim especializando-a.

![Exemplo de herança](/static/image04.jpeg)

*Exemplo de herança em diagrama de classes.*

## Agregação

É um relacionamento do tipo todo-parte, onde existe ainda uma independência entre as classes.

![Exemplo de agregação](/static/image05.jpeg)

*Exemplo de agregação em diagrama de classes.*

O código Java abaixo resume a ligação entre as classes `Curso` e `Professor`:

```java
class Curso {
    private Professor professores[] = new Professor[10];

    public void adicionarProfessor(Professor prof){}
}

class Professor {}
```

## Composição

Também é um relacionamento todo-parte, porém com alto grau de acoplamento entre o todo e as partes.

![Exemplo de composição](/static/image06.jpeg)

*Exemplo de composição em diagrama de classes.*

```java
class Curso {
    private Professor professores[] = new Professor[10];

    public Pedido(){
        for(int i=0; i< professores.length; i++){
            professores[i] = new Professor();
        }
    }
}

class Professor {}
```

## Dependência

Existe dependência do tipo *cliente-fornecedor*, onde uma classe usa outra. Neste caso, uma alteração na classe independente afetará a classe dependente.

![Exemplo de dependência](/static/image07.jpeg)

*Exemplo de dependência em diagrama de classes.*

Todos os conceitos acima apenas resumem bem rapidamente os artefatos usados em diagramas de classes com UML, ou seja, apenas uma breve revisão.

Créditos: Diego Fernando
