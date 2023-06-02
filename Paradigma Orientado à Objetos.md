# O paradigma orientado à objetos

O paradigma orientado à objetos, referido como paradigma OO, é um modelo que tem como conceito fundamental o **objeto**. Muito se confunde o paradigma orientado à objetos com programação orientada à objetos, são conceitos muito relacionados mas ainda assim são diferentes. Conservam-se sim os princípios principais que regem a orientação a objetos:

- A característica mais importante de um software é a encapsulação de objetos.
- A habilidade mais importante para um desenvolvedor é a abstração, capacidade de trazer conceitos do domínio para serem representados de alguma forma concisa no sistema.
- A atividade técnica mais crítica em um projeto de software é a atribuição de responsabilidades a objetos.

>[!info]
>O paradigma OO é presente em todas as áreas da computação. Entre ambos os extremos, é impossível ignorar por completo a existência desse paradigma bem como é impossível utilizar todas as suas definições. Possível é, mas definitivamente imprático.

Para transmitir essas ideias de uma maneira específica é necessário usar uma linguagem adequada. Uma linguagem comumente difundida nesse meio com esse fim é a UML (Unified Modeling Language).
O paradigma não é um processo ou método específico para a modelagem do software em qualquer camada que seja, e sim uma linguagem com vocabulário e regras gramaticais que são boas para descrever sistemas.
A UML permite a representação de muitos conceitos do paradigma OO, mas não todos. A UML não descreve um ciclo de vida OO, não define processos de software, etc.

## Objeto

O objeto, que é o conceito fundamental desse paradigma, possui identidade, propriedades e encapsulação de suas estruturas e funções.

Olhemos primeiro para as **propriedades**. Um objeto tem quatro tipos principais de propriedades:

- atributos: os atributos de um objeto o dão características.
- ligações: objetos podem estabelecer conexões com outros objetos por meio de ligações.
- operações: é como a abstração dos comportamentos/ações realizadas por aquilo que o objeto representa.
- regras: instruções que devem ser obedecidas pelo objeto.

Agora vamos pra identidade. Todo objeto, implicitamente, possui um atributo OID (Object Identifier). Se forem referenciados dois objetos com um mesmo OID em algum modelo, se trata da **mesma instância**.

>[!info]
>Existe uma diferença crucial entre chamar dois objetos de iguais e de idênticos. Objetos **iguais** não possuem nada de diferente entre seus atributos exceto pelo OID. Objetos **idênticos** possuem tudo igual, inclusive o OID. Nesse caso, é possível informar duas coisas: os dois objetos são na verdade um só e é impossível que suas propriedades sejam diferentes uma vez que possuem o mesmo OID.

>[!info]
>OID é um atributo interno do sistema OO que não tem qualquer relação semântica com algo do domínio do sistema. Por exemplo, o OID não é a mesma coisa que o CPF de uma classe Pessoa, apesar de semanticamente fazer sentido que para quaisquer duas instâncias de uma classe Pessoa o CPF não deveria ser igual, bem como o OID.

Um conceito importante sobre os objetos é o estado de um objeto. Esse conceito diz respeito ao conjunto de valores de suas propriedades em dado momento. Uma visão alternativa para o estado do objeto que simplifica o panorama é considerar apenas o conjunto de valores de seus atributos e associações, excluindo o comportamento desse conjunto (algoritmos e regras). Isso se dá em razão do comportamento ser comum a todos os objetos de uma mesma classe.

Agora a encapsulação, o princípio mais importante do paradigma OO. A encapsulação protege o objeto do sistema.

>[!tip]
>O Java, apesar de ser uma linguagem OO, permite violar esse princípio. Isso também é possível na UML.

A encapsulação, teoricamente, envolve o objeto em uma cápsula opaca e indestrutível, que protege-o do sistema. Mas isso é muito estranho quando se leva em conta que uma das propriedades principais dos objetos são as ligações, que permitem ao objeto conectar com os outros. Para contornar essa contradição, se reparte o objeto em dois: a interface, parte apropriada para a interação, que não será encapsulada; e a implementação, que trata dos mecanismos internos do objeto, detalhes que devem ser ocultados e protegidos do restante do sistema.

A interface contém os comportamentos visíveis ao sistema. É importante elucidar que são os comportamentos visíveis ao sistema pois existem comportamentos de um objeto que só são visíveis no próprio escopo, que também são mecanismos internos, aos quais é comumente dado o nome de comportamento privado.

Um objeto pode ter diferentes interfaces para interagir com diferentes objetos do sistema. Isso aprimora uma característica crucial, a usabilidade.

---

# Abstração

Abstrair algo no contexto do software significa trazer algo do domínio da aplicação no mundo real para um modelo de software de forma a representá-lo adequadamente.

Abstrações aplicam princípios essenciais da engenharia de software.

- Dividir para conquistar: princípio utilizado em várias etapas da modelagem do software, está intimimamente relacionado à abstração principalmente no projeto do software, onde o domínio da aplicação é subdividido em problemas menores dos quais são identificadas abstrações que tem seus mecanismos internos encapsulados e seus comportamentos de interação com o sistemas definidos na interface.
- Separação de preocupações: muito semelhante ao tópico anterior, a modularização desse conceito busca dividir um sistema complexo em módulos independentes, no qual cada módula se concentração em uma única preocupação/responsabilidade, vale correlacionar isso com o princípio de responsabilidade única que deve ser exercido por uma classe.
- Ocultação de informações: também relacionado ao primeiro tópico, a encapsulação de informações é natural para proteger o objeto de possíveis anomalias que seriam geradas por interações indesejadas entre objetos do sistema. Faz parte do processo de abstração.

Dentre os tópicos principais sobre astrações OO, pode-se listar:

- classificação e instanciação
- associação e ligação
- agregação e composição
- generalização e especialização

## Classificação

A classificação de objetos reúne as propriedades comuns a diversos objetos. É como se a classe fosse um molde para os objetos. Dito isso, é possível afirmar também que a classe não é um de seus objetos, mas ela de fato é um objeto.

Uma vez definido o molde, é possível criar objetos de acordo com ele indefinidamente sem necessidade de verborragismo. Classes podem ter atributos próprios e métodos próprios.

### Classe abstrata

Uma classe comum pode ser considerada fábrica e armazém de seus objetos por criar novas instâncias e guardá-las, respectivamente. A classe abstrata não é nem fábrica e nem armazém. Então de que ela serve como uma classe? Ela é como um molde base para outros moldes. Apesar de não permitir instanciação, permite especialização, conceito que será visto logo a frente.

>[!info]
>A classe á um meta-objeto

## Instanciação

No processo de instanciação, é criado uma instância do meta-objeto que está realizando esse processo, a qual possui também todas as propriedades deste.

O empacotamento de semelhanças resultantes da abstração facilita muito que a instanciação seja feita por **classes**, seja em tempo de execução ou não. Entretanto também é possível criar instâncias por meio de um objeto prototípico, abordagem muito bem-vinda quando elementos possuem muito mais diferenças do que semelhanças, isso pode ser visto em ferramentas de manipulação de imagens e modelos 3D.


