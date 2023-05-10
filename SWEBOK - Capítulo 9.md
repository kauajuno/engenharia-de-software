O capítulo 9 do SWEBOK  trata de modelos e métodos na engenharia de software. Quatro tópicos principais são cobertos:
- Modelagem
- Tipos de modelos
- Análise de modelos
- Métodos de engenharia de software

# Modelagem

## Princípios de modelagem
Modelagem provém ao engenheiro de software uma abordagem organizada e sistemática para representar aspectos do software. 
Alguns princípios que guiam a modelagem de software são:
- Modelar apenas o essencial: bons modelos não representam todos os aspectos do software de forma robusta, mas em vez disso desenvolvem apenas o essencial a ser entendido, abstraindo os outros detalhes menos importantes.
- Entrega de perspectiva: modelagem fornece perspectivas do software por meio de um conjunto de regras definido para a expressão do modelo em cada perspectiva.
- Comunicação efetiva: modelagem emprega o vocabulário do domínio da aplicação no software, uma linguagem de modelo e expressões semânticas, que possuem significado intrínseco ao contexto.

>[!tip]
>Um modelo é uma abstração ou simplificação de um componente de software.

Utilização de modelos implica em admitir uma série de premissas que se encaixam no contexto no modelo, o que permite que o modelo seja rápido e eficaz para a comunicação a qual é proposto.

## Propriedades e expressão de modelos

Algumas propriedades importantes de um modelo são:

- Completude: essa completude se refere ao quão implementados e verificados o requisito do software estão dentro do modelo.
- Consistência: se refere ao grau em que o modelo apresenta conflito entre requisitos, funções, descrição de componentes e etc.
- Corretude: se refere ao grau de atendimento aos requisitos e ao quão livre de erros o modelo está.

## Sintaxe, semântica e pragmáticos

Modelos podem enganar bastante, o fato de que um modelo é uma abstração do software que pode estar com alguma informação errada ou faltando pode levar o leitor a um falso senso de entendimento do software como um todo a partir de um único modelo. Modelos, ainda mais quando automatizados, devem ser consultados e questionados a fim de chegar sua competude e corretude.

## Pré-condições, pós-condições e invariantes

Ao modelar funções/métodos, é feito um conjunto de premissas sobre o estado do software antes e depois da execução dessa função/método.

- Pré-condições: conjunto de condições que devem ser atendidas para a execução.
- Pós-condições: conjunto de condições que serão verdadeiras após a execução.
- Invariantes: condições que irão persistir mesmo com a execução.

# Tipos de modelos

Um modelo **típico** é composto de um agregado de submodelos, no qual cada submodelo é uma descrição parcial de algo e é criado para um propósito específico. Esse agregado pode empregar diversas linguagens de modelagem de uma vez só.

## Modelos de Informação

Centrado principalmente em dados e informação. Um modelo de informação define uma série de conceitos, propriedades e relações de entidades de dados. Um exemplo de modelo de informação é o diagrama entidade-relacionamento.

## Modelos comportamentais

Modelos comportamentais geralmente tomam três formas diferentes:

- máquinas de estado
- modelos de fluxo de controle
- modelos de fluxo de dados

Diagramas de casos de uso e diagramas de estado são bons exemplos de modelos comportamentais.

## Modelos de estrutura

Modelos que ilustram composição física ou lógica dos vários componentes do software, podendo apresentar o design/arquitetura de um sistema sobre algum aspecto. Diagramas de componentes e diagramas de classes são exemplos de modelos de estrutura.

# Análise de Modelos

## Análise de completude

Modelos devem ter a completude checada por uma ferramenta de modelagem que usa técnicas como análise estrutural e análise de acessibilidade em espaço de estados (que confere se todos os caminhos do modelo podem de fato ser alcançados). Também é possível revisar os modelos manualmente por meras inspeções ou outras técnicas de revisão. Erros indicados a partir disso indicam um caminho para correções do modelo.
Exemplo de ferramenta automatizada para análise: 

## Análise de consistência

Análise de consistência também pode ser feita nas próprias ferramentas de modelagem ou manualmente. Possíveis passos para a análise de consistência de um modelo incluem a verificação do escopo, verificação da estrutura, identificação de conflito de requisitos, 

## Análise de corretude

Análise de corretude envolve verificar a sintática do modelo bem como a corretude semântica. Esse processo pode ser feito manualmente mas frequentemente irá envolver ferramentas automatizadas de teste. Trazendo exemplos mais sólidos, na área do desenvolvimento o Selenium é uma ferramenta de automação de testes para corretude.

## Rastreabilidade

Rastreabilidade pode parecer um tópico perdido em meio às análises mas ela também é uma forma importante de se analisar. Rastreabilidade diz respeito à capacidade de rastrear um modelo e seus relacionamentos com outros modelos e artefatos componentes do software. Isso é importante para garantir o atendimento dos requisitos e mostrar como eles se ligam e ficam de acordo com os modelos gerados no ciclo de vida do software. Um exemplo de ferramenta utilizada com propósito de manter rastreabilidade é o [IBM Rational DOORS](https://www.ibm.com/docs/pt-br/elms/ermd/9.6.1?topic=overview-rational-doors).

## Análise de interação

Essa análise que não é competente à um aspecto específico do software como um todo foca na comunicação/fluxo de controle entre as entidades para realizar uma tarefa específica. Essa análise examina o comportamento dinâmico das interações entre diferentes entidades do software.

# Métodos na Engenharia de Software

Métodos em ES fornecem formas organizadas e sistemáticas para lidar com o desenvolvimento de um software. Existem numerosos métodos mas existem quatro classes de métodos principais nas quais é possível encaixá-los:

- Métodos de heurística: métodos baseados em experiência que vêm sendo amplamente praticados na indústria de software. Esse tópico se estende para outros três:
	- Análise estruturada e métodos de design
	- Métodos para modelagem de dados
	- Análise OO e Métodos de Design
- Métodos formais: métodos formais são métodos usados para especificar, desenvolver e verificar o software por meio da aplicação de notaçãões e linguagens rigorosamente baseadas em matemática.



