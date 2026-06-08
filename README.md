# Treinamento-de-IA-via-NotebookLLM
Projeto de estudo com o objetivo de explorar a capacidade da IA de aprendizagem da Google, NotebookLM, através da definição de um tópico e disponibilização de fontes. Neste projeto contará com:
* Teste das capacidades de raciocínio e interpretação com base nos conteúdos disponibilizados
* Miniguia de estudo (Produzido pelo NotebookLM)
* Glossário para termos técnicos (Produzido pelo NotebookLM)

<h3>Assunto: Guia de estudo para aprender C# com foco em uso no Unity para programação de jogos </h3>
<h3>Fontes:</h3> 

  * [**Documentação oficial**](https://docs.unity3d.com/Manual/index.html)
  * [**Livro 1**](/Livros_Fontes/C_Language_Specification.pdf)
  * [**Livro 2**](/Livros_Fontes/Pro_Unity_Game_Development_with_C.pdf)
  * [**Livro 3**](/Livros_Fontes/game-programming-with-unity-and-c-a-complete-beginners-guide.pdf)

## Documentação dos Prompts
1. **"Com base exclusivamente nos documentos fornecidos sobre Unity e .NET, qual é a versão do framework recomendada para novos projetos e por quê?"**:
 
O objetivo desse teste foi para verificar a capacidade do NotebookLM navegar pelo material e verificar se ele está consultando corretamente as fontes. O resultado foi satisfatório.

2. **"Mudei meu projeto Unity para rodar em .NET Framework antigo porque li nas fontes que o IL2CPP só funciona com ele. Está correto?"**:

Essa pergunta teve um objetivo de avaliar o senso crítico, se o NotebookLM apenas concordava com tudo que o usuário diza ou se buscaria e responderia corretamente com base nos materiais. A resposta foi bem educada com explicações bem baseadas, e ainda deu uma recomendção de como se deve tratar novos projetos para garantir sempre uma boa compatibilidade.

3. **Explique a tabela de compatibilidade da API .NET do Unity, mas faça isso como se você estivesse explicando para uma criança de 10 anos que quer criar um mod de Roblox.**:

Essa pergunta mirou na capacidade do NotebookLM em interpretar o assunto disposto e conseguir fazer uma analogia simplificada, transformando termos técnicos em de fácil entendimento. A resposta cumpriu o que foi pedido com uma explicação bem facilitada. 

## Miniguia de estudo
### 1. Fundamentos e Ambiente de Desenvolvimento
* **Instalação e Ferramentas:** O desenvolvimento começa com o Unity Hub, que gerencia diferentes versões da engine e projetos. O Visual Studio Code é recomendado como editor de código leve e extensível para C#.
* **A Engine Unity:** O ambiente é composto por janelas essenciais: Hierarchy (lista de objetos na cena), Scene (visualização 3D/2D), Inspector (propriedades dos objetos) e Project (arquivos de ativos).
* **GameObjects e Componentes**: Tudo em uma cena é um GameObject, que serve como um contêiner para Componentes (como Transform, Camera e Light) que definem sua funcionalidade.
* **Prefabs:** São "blueprints" ou modelos de objetos que permitem criar instâncias reutilizáveis; alterações no Prefab original podem ser aplicadas automaticamente a todas as suas instâncias.
### 2. Linguagem de Programação C#
* **Natureza da Linguagem:** O C# é uma linguagem fortemente tipada, moderna e orientada a objetos.
* **Sistema de Tipos:** Divide-se em tipos de valor (ex: int, float, bool, structs) e tipos de referência (ex: class, interface, array, delegate).
* **Estrutura de Programação:** Organiza-se através de Namespaces (hierarquia de organização), Classes (moldes para objetos) e Membros (campos, métodos e propriedades).
* **Lógica e Controle de Fluxo:** Utiliza instruções como if, switch para decisões e while, for, foreach para repetições.
### 3. Scripting no Unity
* **MonoBehaviour:** É a classe base da qual a maioria dos scripts deriva, permitindo que o código seja anexado como componente a um GameObject.
* **Métodos de Evento:** Os principais são o Start(), chamado uma vez no início, e o Update(), chamado a cada quadro (frame).
* **Comunicação entre Objetos:** Pode ser feita via GetComponent<T>() para acessar outros componentes ou através de mensagens como SendMessage e BroadcastMessage.
* **Singletons:** Padrão de projeto usado para garantir que uma classe (como o GameManager) tenha apenas uma instância ativa e globalmente acessível.

### 4. Sistemas de Jogo e Dinâmicas
* **Física e Colisões:** O Unity utiliza Rigidbodies para simulação física e Colliders para detectar contatos; o evento OnTriggerEnter é usado para detectar quando objetos se atravessam.

* **Inteligência Artificial (IA):** Implementada frequentemente através de Máquinas de Estado Finitas (FSM), onde o inimigo alterna entre estados como Patrulhar, Perseguir e Atacar.

* **Navegação:** O sistema de NavMesh permite que personagens inteligentes encontrem caminhos e evitem obstáculos no cenário.

* **Interface de Usuário (GUI):** Composta por elementos como Canvas, botões e textos, podendo ser configurada para ser relativa ao tamanho da tela (resolução independente).
### 5. Tecnologias Modernas (Unity 6 e Otimização)
* **Inovações do Unity 6:** Foco em desempenho de renderização, ferramentas de IA (Unity AI) para geração de código e ativos, e avanços em multiplayer.

* **Otimização:** O uso do C# Job System, Burst Compiler e a renderização via URP (Universal Render Pipeline) são fundamentais para alta performance em múltiplas plataformas.

* **Dados Persistentes:** O salvamento de progresso pode ser feito via classe PlayerPrefs (para dados simples) ou serialização em arquivos XML/JSON (para estados de jogo complexo

## Glossário
Com base nos materiais fornecidos, este glossário define os termos técnicos fundamentais apresentados no guia de aprendizagem de C# para Unity.

### A
*   **API Compatibility Level**: Uma configuração no Unity que define quais recursos do framework .NET estão disponíveis para o projeto (ex: .NET Standard ou .NET Framework).
*   **Array (Arranjo)**: Uma coleção de itens do mesmo tipo armazenados em índices específicos, começando pelo índice 0.
*   **Asset (Ativo)**: Qualquer arquivo utilizado no projeto do jogo, como modelos 3D, sons, imagens ou scripts.
*   **Attribute (Atributo)**: Metadados inseridos entre colchetes `[]` antes de uma declaração (como `[Header]` ou `[HideInInspector]`) para modificar como o Unity exibe ou processa essa definição.

### B
*   **Bool (Booleano)**: Um tipo de dado que representa apenas dois valores lógicos: `true` (verdadeiro) ou `false` (falso).
*   **Build**: O processo de converter o projeto Unity em um aplicativo executável independente para uma plataforma específica (Windows, Android, etc.).

### C
*   **Class (Classe)**: O "molde" ou modelo fundamental do C# que combina dados (campos) e ações (métodos) em uma única unidade.
*   **Collider (Colisor)**: Um componente que define a forma física de um objeto para detecção de colisões no sistema de física.
*   **Component (Componente)**: Uma unidade de funcionalidade (como um Script, Transform ou Light) anexada a um GameObject.
*   **Coroutine (Corotina)**: Um método especial que pode pausar sua execução (`yield`) e retomá-la em quadros (frames) subsequentes, útil para ações temporizadas.

### D
*   **Dictionary (Dicionário)**: Uma coleção de dados organizada em pares de "chave e valor", permitindo buscas rápidas por uma chave específica.

### E
*   **Enum (Enumeração)**: Um tipo de valor que declara um conjunto de constantes nomeadas, facilitando a leitura do código.

### G
*   **GameObject**: O objeto fundamental em uma cena do Unity; funciona como um contêiner para componentes.

### H
*   **Hierarchy (Hierarquia)**: A janela do editor que lista todos os GameObjects presentes na cena ativa.

### I
*   **IL2CPP**: Um backend de script que converte o código CIL em C++ para compilação nativa, oferecendo alta performance.
*   **Inheritance (Herança)**: Um mecanismo de Orientação a Objetos onde uma classe "filha" herda propriedades e comportamentos de uma classe "pai".
*   **Inspector (Inspetor)**: Janela onde se visualizam e editam as propriedades de GameObjects e componentes selecionados.
*   **Instantiate (Instanciar)**: O ato de criar uma nova cópia de um objeto ou Prefab em tempo de execução através de código.

### L
*   **List (Lista)**: Uma coleção dinâmica de itens que pode crescer ou diminuir de tamanho conforme necessário.

### M
*   **Method (Método)**: Um bloco de código nomeado que executa uma tarefa específica quando chamado (também conhecido como função).
*   **MonoBehaviour**: A classe base da qual quase todos os scripts do Unity derivam, permitindo que o script seja anexado como componente e use eventos como `Start` e `Update`.

### N
*   **Namespace (Espaço de Nomes)**: Um sistema de organização de código que agrupa classes relacionadas (ex: `UnityEngine` ou `System.Collections`).

### P
*   **Parenting (Parentesco)**: O sistema de anexar um GameObject ("filho") a outro ("pai"), fazendo com que o filho siga a posição, rotação e escala do pai.
*   **Prefab**: Um modelo ou "blueprint" reutilizável de um GameObject configurado, que pode ser replicado em várias cenas.
*   **Property (Propriedade)**: Um membro que atua como um híbrido entre variável e método, usando acessores `get` e `set` para ler ou gravar dados.

### Q
*   **Quaternion**: O tipo de dado matemático complexo usado pelo Unity para representar e processar rotações 3D internamente.

### R
*   **Raycast**: Uma operação de física que "dispara um raio" de um ponto em uma direção para detectar colisões com objetos no cenário.
*   **Rigidbody**: Componente que adiciona comportamento físico a um objeto, permitindo que ele reaja à gravidade e forças.

### S
*   **Singleton**: Um padrão de projeto que garante que exista apenas uma única instância ativa de uma classe na memória durante o jogo.

### T
*   **Transform**: O componente essencial presente em todos os GameObjects que define sua posição, rotação e escala no espaço.

### U
*   **Update**: Um método de evento interno chamado automaticamente pelo Unity uma vez a cada quadro processado pelo computador.

### V
*   **Variable (Variável)**: Um local nomeado na memória para armazenar dados de um tipo específico.
*   **Vector3**: Uma estrutura que armazena três valores numéricos (X, Y, Z), usada para representar posições, direções ou escalas em 3D.

## Prompts reutilizáveis
1. **Para caso você esteja com dificuldade em entender um assunto específico:** "Explique [assunto desejado], mas faça isso como se você estivesse explicando para uma criança de 10 anos que quer criar um mod de Roblox[Ou algum outro jogo/analogia que melhor sirva para você]."
2. **Para caso queira estruturar um cronograma mais personalizado:** "Tenho [Horas por dia que você tem dísponivel], crie um cronograma de estudo no estilo de um [Jogo: caso queira algo mais gameficado, Livro de recitas: caso queira algo mais estrutural]"
