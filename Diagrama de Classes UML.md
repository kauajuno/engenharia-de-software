#uml 

---

# Propósito

O diagrama de classes UML serve muito bem ao propósito de apresentar software OO de uma maneira visual e holística, permitindo a visualização das relações entre as classes de um sistema.

# Classe

A classe corresponde à abstração de algo no domínio do problema. Ela descreve as características desse algo por meio dos atributos, e ações por meio de métodos (getters e setters são discutíveis).

![[uml-class-example-animal.png]]

## Atributos

Os atributos descrevem características da entidade abstraída para o modelo. No contexto do software no qual essa modelagem irá ocorrer, é importante saber dizer o **tipo** desse atributo. Alguns tipos comuns são: `string`, `int`, `bool`, `float`, etc.

>[!info]
>Alguns atributos podem ser instâncias de outra classe ou até mesmo da própria classe.

## Métodos

Os métodos descrevem o comportamento da entidade abstraída para esse modelo. No contexto do software no qual essa modelagem irá ocorrer, é importante saber dizer o que esse comportamento tem como pré-condições para ocorrer (muitas vezes isso se transcreve na forma de **parâmetros de entrada**) e se ele gera algum retorno, e caso sim, o **tipo** desse retorno.

## Grau de visibilidade

O grau de visibilidade de um atributo diz respeito ao nível de exposição de um atributo ou método ao restante do sistema / por quem ele pode ser acessado. Na UML, existem 4 graus de visibilidade:

- Private `-` -> Atributos e métodos privates são visíveis somente no escopo da própria classe, portanto só podem ser acessados pela própria classe. Muito usado para designar mecanismos internos que não são de interesse a qualquer outra entidade do sistema.
- Public `+` -> Atributos e métodos públicos podem ser acessados em todo o sistema.
- Protected `#` -> Atributos e métodos protected só podem ser vistos no escopo da própria classe e das classes que herdam a ela.
- Package `~` -> Atributos e métodos package podem ser vistos por todas as classes que pertencem à package na qual se situa. Muito situacional, esse grau de visibilidade não é tão visto assim.

# Relacionamentos

Naturalmente, classes se relacionam pra criar um sistema que possibilita a interação entre diferentes entidades. Seria praticamente impossível desenvolver software OO se classes fossem completamente cobertas pela camada opaca e indestrutível que conhecemos por proteger os mecanismos internos de uma classe. Felizmente classes possuem interfaces para interação com o restante do sistema.

## Herança

O que provavelmente é o relacionamento mais reconhecido, até mesmo por ser um pilar da programação orientada à objetos, é a herança. A herança permite que uma classe herde outra classe, recebendo todos os seus atributos e métodos, podendo sobrescrevê-los se necessário.

![[exemplo-uml-heranca-animal.png]]

Nesse caso, tanto a classe Tartaruga quanto a classe Quokka recebem todos os atributos e métodos da classe animal.

## Associação

Digamos que Quokkas gostem de comer cenouras (fato não comprovado cientificamente). E digamos também que isso é uma informação crucial pro nosso sistema de exemplo, então vamos modelar isso:

![[uml-exemplo-associacao.png]]

Associações são relacionamento simples que descrevem alguma interação entre duas classes do sistema. Para associar Quokka à Cenoura, bastou uma simples linha, essa simples linha representa uma associação.

## Agregação

Agregação é o primeiro dos dois tipos de relacionamento parte-todo que são representados especialmente na UML. A agregação ajuda a representar um relacionamento no qual várias instâncias de uma classe compõem uma outra classe. Os elementos que compõem essa classe são independentes dela, e podem existir sem que ela exista.

Por exemplo, um bando de tartarugas é composto por várias tartarugas, mas uma tartaruga pode viver sem estar em um bando. Vamos modelar isso:

![[uml-exemplo-agregacao.png]]

## Composição

Se a agregação é a relação parte-todo na qual a parte pode existir fora do todo, a composição é aquela na qual a parte **não pode** existir fora do todo. Por exemplo, em uma casa, há banheiro e cozinha, mas se a casa deixar de existir, também deixarão de existir o banheiro e a cozinha:

![[uml-exemplo-composicao.png]]