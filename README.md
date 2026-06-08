# Treinamento-de-IA-via-NotebookLLM
Projeto de estudo com o objetivo de explorar o poder de IAs de aprendizagem

<h3>Assunto: Guia de estudo para aprender C# com foco em uso no Unity para programação de jogos </h3>
<h3>Fontes:</h3> 

  * [**Documentação oficial**](https://docs.unity3d.com/Manual/index.html)
  * [**Livro 1**](/Livros_Fontes/C_Language_Specification.pdf)
  * [**Livro 2**](/Livros_Fontes/Pro_Unity_Game_Development_with_C.pdf)
  * [**Livro 3**](/Livros_Fontes/game-programming-with-unity-and-c-a-complete-beginners-guide.pdf)

## Documentação dos Prompts:
1. **"Com base exclusivamente nos documentos fornecidos sobre Unity e .NET, qual é a versão do framework recomendada para novos projetos e por quê?"**:
 
O objetivo desse teste foi para verificar a capacidade do NotebookLM navegar pelo material e verificar se ele está consultando corretamente as fontes. O resultado foi satisfatório.

2. **"Mudei meu projeto Unity para rodar em .NET Framework antigo porque li nas fontes que o IL2CPP só funciona com ele. Está correto?"**:

Essa pergunta teve um objetivo de avaliar o senso crítico, se o NotebookLM apenas concordava com tudo que o usuário diza ou se buscaria e responderia corretamente com base nos materiais. A resposta foi bem educada com explicações bem baseadas, e ainda deu uma recomendção de como se deve tratar novos projetos para garantir sempre uma boa compatibilidade.

3. **Explique a tabela de compatibilidade da API .NET do Unity, mas faça isso como se você estivesse explicando para uma criança de 10 anos que quer criar um mod de Roblox.**:

Essa pergunta mirou na capacidade do NotebookLM em interpretar o assunto disposto e conseguir fazer uma analogia simplificada, transformando termos técnicos em de fácil entendimento. A resposta cumpriu o que foi pedido com uma explicação bem facilitada. 

## Miniguia de estudo: 
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
