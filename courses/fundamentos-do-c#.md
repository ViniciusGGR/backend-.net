# Fundamentos do C#

---

## Linguagens e Compiladores:

### Linguagens de programação

Uma _linguagem de programação_ é a forma **comunicação** como humanos dizem para o computador executar algo.

Computadores utilizam o formato **_binário_**, 0s e 1s para realizar operações executadas dentro do precessador/CPU, GPU, Memória...

As **Linguagens de Programação** LPs, fazem o intermédio.
- O que os devs escrevem será traduzido para uma linguagem binária (linguagem de máquina).
    - Resumo: Arquivo de texto que humanos conseguem ler, que é traduzido para binário, assim o computador consegue ler/executar esse arquivo.
- O processo de "tradução" é conhecido como **_compilação_**.
- **Obs**: Existem várias **linguagens de programação**.
    - Cada linguagem tem seu compilador.
    - Cada compilador trabalha de uma forma.

> **_Compilador_**: Agente que executa a compilação, que é a transformação do texto escrito para binário (0 e 1).

### Alto e baixo nível

Ao enviar uma instrução ao computador, se está falando em **_nível de máquina_ (baixo nível)**.
- Instruções sempre serão em formato binário.

Alto nível está mais próximo dos usuários/desenvolvedores, e baixo nível está mais próximo do CPU/GPU, que é as instruções em binário.

Quanto mais detalhada a necessidade de mandar uma instrução para o processador, mais baixo será o nível.

As linguagens mais modernas como _C#_ e _Java_ são consideradas de **alto nível**.
- Alto nível: Favorece mais os desenvolvedores do que o processador.

> **_Linguagens de alto nível fornecem um acesso à tudo que é preciso a nível de hardware já pronto_**.

### Linguagem compilada e interpretada

**Linguagens compiladas**:

Uma linguagem é compilada quando existe o processo de compilação.
- Compilação: Conversão de um arquivo de texto (de fácil entendimento para humanos) para binário (0s e 1s).

**Linguagens interpretadas**:

São arquivos de texto, que _não são convertidos para binário_.
- Arquivos lidos e interpretados por um **intérprete**.
- A interpretação/leitura do arquivo é feita em **_tempo de execução/real_**.
    - Exemplo de uma linguagem interpretada: **JavaScript**.

> **Tempo de execução**: É o que acontece durante a execução do código pelo computador/interpretador.

As linguagens interpretadas, no caso o JavaScript:
- Os navegadores é escrito em uma linguagem de alto nível.
- Os navegadores possuem um **interpretador**.
- Lê e executa um arquivo de texto JavaScript.

### Compilada e interpretada

Linguagens Compiladas e Interpretadas não mudam muito em relação a sintaxe, mas sim na sua execução por "baixo dos panos".

Prós das _Linguagens Interpretadas_:
- Não precisa ser compilada.
    - Não existe tempo de compilação.
- Correções mais fáceis de serem executadas.
- Mais simples de serem distribuídas.
    - São "Arquivos estáticos", basta copiar os arquivos para o local desejado que tudo estará pronto/configurado.
        - Não precisa ser traduzida para uma _linguagem de máquina_ antes da execução.

Contras das _Linguagens Interpretadas_:
- Detecção de erros com mais dificuldade.
    - Os erros só aparecem em _tempo de execução/leitura_.
- Tamanho final das aplicações são maiores.
- A otimização da execução dos arquivos interpretados é menor.
- Tem múltiplos arquivos.

Prós das _Linguagens Compiladas_:
- Tempo de compilação.
    - Detecção de erros mais rápida.
    > **Tempo de compilação**: _É tudo o que acontece enquanto o programa está sendo compilado._
- Menor tamanho das aplicações.
    - Aplicações .NET tem o arquivo _exe/dll_ no Windows, e no Mac/Linux um arquivo _dll_, que são arquivos bem compactados.
- Maior otimização da execução.
- Apenas um arquivo final por projeto.

Contras das _Linguagens Compiladas_:
- Precisa de um compilador.
    - Precisa para compilar/transformar a linguagem para baixo nível, que o computador entenda. 
- Pode ser mais burocrática.

### Tipagem de dados

O que é uma linguagem "_tipada/fortemente tipada_"?

- Uma linguagem tipada obriga o desenvolvedor a **especificação do tipo de dado da informação** armazenada em qualquer variável.
- O dev tem uma _liberdade menor_, pois não será possível criar qualquer tipo de informação na aplicação.
- O sistema fica muito mais otimizado com a tipagem de dados, pois o sistema já sabe o local na memória onde será armazenado esses tipos de informação.

> **Tipo de Dado**: Um _tipo de dado_ define o formato de uma informação, onde se define por exemplo que aquela informação é um número, uma letra, uma cadeia de caracteres e assim por diante.

Exemplo de tipagem com C#:

```
int age = 18; // OK
int age = 18.2 // ERRO
int age = "18"; // ERRO
int age = 'a'; // ERRO
```
- O ``int`` define que a variável **age** receberá um valor **_inteiro_**, e somente um valor _inteiro_ sem exceções.

> **O C# é uma linguagem de alto nível, compilada e fortemente tipada**.

- A tipagem de dados serve para definir tipos e padronizar os dados.
    - Tanto para o processador/memória, quanto para os desenvolvedores.
- Tipar traz uma melhor otimização.
- O ``let`` utiliza sempre o mesmo tamanho de alocação da memória, não tendo assim uma otimização.

Otimização da tipagem no C# por exemplo:
- int => 32 bit
- float => 32 bit
- double => 64 bit
- decimal => 128 bit

### Revisão

O que foi apresentado no módulo:
- Linguagens Tipadas e Não Tipadas.
- Linguagens Compiladas e Interpretadas.
- Linguagens de Alto e Baixo nível.
- Compiladores.

---

## C#:

### Por que utilizar C#?

**_#_** - Sharp/Tralha/Hashtag...

C# é uma linguagem de programação **tipada**, **compilada** e **gerenciada**. Foi criada em meados de 2001 por _Anders Hejlsberg_, sendo a principal linguagem da Microsoft.
- Anders Hejlsberg também é responsável pelo Delph e TypeScript.

O que o C# trás de vantagens:
- Mercado.
- Comunidade.
- Linguagem Orientada a Objetos.
- Maturidade.
- Linguagem completa.
    - Sendo utilizado para Web, Mobile, Desktop, IA, Machine Learning, Desenvolvimento de jogos...
- Microsoft por trás.

### C# como primeira linguagem

- O C# é focada em OOP - Orientação a Objetos (Base da programação).
    - Também pode-se utilizar o Paradigma _funcional_.
    - **Nota**: O C# te "_obriga_" a utilizar o paradigma de Orientação a Objetos.
- OOP dá a base para aprender coisas novas.

**Dica**: Consolide o básico, assim você será capaz de aprender coisas novas com mais facilidade, não terá resistência a mudanças, pois você terá a capacidade de migrar de tecnologia de uma forma mais simples.

### Código gerenciado

Uma **_linguagem gerenciada_** tem sua execução dependente de um gerenciador.

O **Gerenciador** do C# é conhecido como **_Runtime_**, sendo o item que gerencia os programas escritos em C#.
- No C# este **Runtime** se chama **_CLR_** ou **_CLR Runtime_**. 
- O Runtime gerencia memória, segurança, entre outros recursos básicos.

> **CLR:** CLR é uma sigla para _Common Language Runtime_ ou **gerenciador de linguagem comum**.

Um gerenciador como o Runtime, permite que nós desenvolvedores possamos interagir menos ou quase não interagir com recursos de máquina. O gerenciador também torna o desenvolvimento mais rápido.

### Compilação e gerenciamento

Compilação e Gerenciamento no C#:
- A Microsoft possui outras linguagens como VB.NET, F#, Cobol.NET, sendo preciso ser todas mantidas. Com manutenção de códico, sendo correções de bugs e afins.
- O ecossistema de desenvolvimento da Microsoft foi criado e pensado para dar **Suporte a várias linguagens**.
    - Se cada _linguagem da Microsoft_ tivesse um gerenciador, seria muito complicado o suporte a várias linguagens.

O ecossistema criado pela Microsoft tem cada compilador separado um do outro. Cada linguagem tem seu compilador (ou mais de uma linguagem).

A compilação **_inicial_** não gera o código final, no caso o binário. Para manter somente **um** compilador final, a Microsoft criou uma linguagem intermediária, conhecida como "_Intermediate Language_" (**IL** - Linguagem intermediária).

Quando realizada a compilação do código C#, esse código é "_traduzido_" para uma linguagem intermediária, e somente depois é **compilado**. Esse processo permite que tenha somente um gerenciador para as linguagens, e permite o uso de diferentes tipos de arquivos em um único projeto.

### IL

**Código em C#, VB.NET, F#, Cobol.NET** -> são traduzidos para a -> **Intermediate Language "_IL_"** -> depois será gerado um -> **Código Binário**.

- Embora as compilações sejam diferentes, o _gerenciamento_, _alocação de memória_ e _execução de instruções no processador_ é o **mesmo**.
- O CLR recebe um código e compila ele para IL (Intermediate Language).
- Pode-se ter arquivos C# (.cs) e VB.NET (.vb) no mesmo projeto.
    - **Nota**: Isso _nunca_ acontecerá no mesmo arquivo.
- O resultado da compilação do **IL** é sempre o mesmo.

**Dica**: O processo de conversão do IL para binário é conhecido como **JIT**.
- JIT: Sigla para _Just in Time_.

### Revisão

- C# é uma linguagem completa, popular é tem muito material.
- É uma linguagem desafiadora, mas que traz como benefício muito aprendizado.
- O C# é uma linguagem fortemente tipada, de alto nível, compilada e gerenciada.
- O C# é compilado inicialmente para IL - _Intermediate Language_.
    - Depois o CLR/Runtime compila para código de máquina/binário, executa e gerencia.
- **IL** é a linguagem intermediária na qual todas linguagens da Microsoft são compiladas.

---

## Frameworks:

### Frameworks

O **Framework** é uma estrutura, um alicerce para a construção de aplicações.
- Os Frameworks são _conjuntos de bibliotecas_. São utilizados como base para a construção de aplicações.
- Os Frameworks ajudam muito, pois com eles não é necessário começar tudo do zero.
- Framework é um conceito existente em diversas tecnologias.
- **_.NET_** é um Framework da Microsoft.

A ideia do _.NET Framework_ é trazer recursos comuns já prontos, validados e testados.
- Esses "recursos" poupam muito tempo.

O .NET foi criado em 2001, "junto" ao C#.

### .NET Framework

.NET Framework:
- O Framework **``.NET``** teve sua primeira versão em 2001, sendo chamado de ".NET Framework".
- .NET recebeu as versões 1.0, 1.1, 2.0, 3.0, 3.5, 4.x...
- O ".NET Framework" pode ser instalado ``Side-by-side``, podendo assim ter duas versões do ".NET Framework" uma ao lado da outra.
- É compativel somente com o Windows.
- É considerado legado.

> **Legado**: Softwares legados são considerados assim, quando atingem uma certa idade.

### .NET Core

.NET Core:
- ".NET Core" é uma versão moderna do Framework ".NET Framework".
- Lançado em meados de 2015.
- O Framework foi lançado especialmente para dar suporte a outros SOs, como Linux e Mac.
- As primeiras versões do Framework continham apenas o básico.
    > _Core_ significa **núcleo**, ou seja, o essencial.
    - O Framework _.NET Core_ foi totalmente reescrito.
    - O _.NET Core_ tem uma ótima **_``retro compatibilidade``_** com o _.NET Framework_.
- Versão 3.1/3.2 está bem estável.
    - Essas versões são as recomendações da Microsoft.
    - Essas versões trouxeram muitas melhorias de **performance**.
- Versões do .NET Core:
    - 1.0, 1.1, 2.0, 2.1, 3.0, 3.1...
- O Framework possui instalação ``Side-by-side``, podendo assim ter duas versões do ".NET Core" uma ao lado da outra.

### .NET Standard

_Standard_ = **Padrão**

O .NET Framework e o .NET Core coexistem, podendo ser instalados juntos, e utilizados no mesmo projeto.

O **.NET Standard** garante que o código rode em ambos, tanto no .NET Framework, como no .NET Core. O **.NET Standard** é considerado a _"intersecção" entre os dois frameworks_.

O .NET Standard não é um framework, e sim um contrato/definição.
- É conhecido como uma **Surface API**.
- Garante que tudo o que foi escrito será compatível com ambos frameworks.

### .NET 5

O _.NET 5_ é a **Unificação dos Frameworks** - .NET Core e .NET Framework.
- Não faz sentido ter dois frameworks, por isso surge o **.NET 5**, para realizar essa unificação.

### LTS

Realese/Lançamento - É uma versão nova de algo, por exemplo, realeses do Windows, Mac, Linux...

.NET Framework:
- Não possuia uma data de lançamento programada.
.NET Core:
- Lançamentos (Realeses) semestrais.
.NET 5...
- Lançamentos anuais.

**Nota**: Realeses com um espaço de tempo menor, e com uma quantidade menor de alterações, contribui para uma absorção mais rápida da nova versão por seus usuários.

Sigla **LTS**:
- Sigla para _Long Term Support_:
    - Suporte de longa data.
- Versões **LTS** do .NET Framework:
    - Todos eram _LTS_.
- Versões **LTS** do .NET Core:
    - Versões com final 1.
    - 1.1, 2.1, 3.1...
- Versões **LTS** do .NET 5:
    - Versões Maiores.

**Dica**: Sempre opte por utilizar versões _LTS_ para projetos em produção.

### Versionamento

Versionamento de Software:
- O _versionamento_ é definido por uma **Versão Semântica**. Essa _versão semântica é **divida em fases**.
    - Fases: Alpha, Beta, Realese Candidate, Final.
        - **Alpha**: Versão inicial/esboço, está muito longe de uma versão final.
            - Em uma versão _Alpha_, ainda não se sabe como vão ser as coisas. Muita coisa pode mudar.
            > **Alpha** => 0.0.1-a1
            - _a1_ - Alpha 1.
        - **Beta**: É uma versão de testes, já tem algumas coisas funcionando.
            - Em uma versão _Beta_, já se tem ideia da estrutura, mas as coisas ainda podem mudar.
            > **Beta** => 0.0.2-b1
            - _b1_ - Beta 1.
        - **Realese Candidate**: É uma versão candidata a ser uma _versão final_ da aplicação, já tem os bugs corrigidos, nomes definidos...
            - Uma versão _Realese Candidate_ é um "Candidato a versão final".
            > **Realese Candidate** => 1.0.0-rc1
            - _rc1_ - Realese Candidate 1.
        - **Final**: "Última" versão do Software.
            > **Final** => 1.0.0
    - **Nota**: Todo o versionamento de software é dado por números e letras.
    - **Dica**: Normalmente _Alpha_ e _Beta_ tem versões menores que **1.0.0**.
        - A numeração é divida em três partes:
            - **Major**: É sempre o primeiro número, ou seja, sempre é a realese maior.
                - **3**.1 - O número 3 é o _Major_.
                - Quando o **Major** é alterado, significa que houve uma _grandes alterações_ na aplicação.
                > O **Major** pode conter incompatibilidade com versões anteriores, chamadas de _Breaking Changes_.
            - **Minor**: É o segundo número, ou seja, o primeiro número depois do ponto.
                - 3.**1** - O número 1 é o _Minor_.
                - Quando o **Minor** é alterado, significa _pequenas alterações_ na aplicação.
                > O **Minor** possui mudanças mas é totalmente compatível com versões anteriores, chamada de _Backward Compatibility_.
            - **Patch**: É o terceiro número, ou seja, o primeiro número depois do segundo ponto.
                - 3.1.**2** - O número 2 é o _Patch_.
                - Normalmente o _Patch_ é para correções de bugs da versão atual do software.
                > O **Patch** é para correções de bugs e outros itens simples.

### Runtime e SDK

O Runtime faz o gerenciamento/execução da aplicação, sendo exigido para rodar o código em C# compilado.

Em resumo, as aplicações .NET são dividas em 3:
- ASP.NET é uma tecnologia dentro do .NET para Aplicações Web.
- WPF e Winforms para aplicações Desktop.
- .NET Core para qualquer outra aplicação
    - Console, Batch, Serviço.
    - Não possui uma interface por exemplo.
- Cada um desses serviços dentro do .NET, possuem diversas versões, sendo assim, a versão tem que ser compatível com a versão utilizada durante a codificação.

O Runtime é responsável por rodar/executar as aplicações. O Runtime tem assim um tamanho menor, otimizado para execução.

**SDK** - Sigla para **_Software Development Kit_**.
- Kit para desenvolvimento de software.

O SDK traz o compilador, suporte a sintaxe do C#, várias ferramentas qua auxiliam durante o desenvolvimento.
- O tamanho do SDK é muito maior do que o do Runtime, pois o Runtime só executa a aplicação. Já o SDK permite o desenvolvimento de softwares, utilizando o C#, ASP.NET Core...
- O SDK possui todo o necessário para desenvolver uma aplicação.
- O SDK já vem com o Runtime integrado.
    - Não é possível instalar o SDK sem o Runtime, mas é possível instalar o Runtime sem o SDK.

**Dica**: Não é preciso utilizar o SDK em produção, pois para executar só é preciso o Runtime do .NET.

### Revisão

- Frameworks são estruturas prontas, que ajudam a otimizar/economizar tempo e ajudam a diminuir os riscos dos projetos.
- .NET Framework é o legado.
- .NET Core é o atual.
- .NET 5 é o futuro.
- .NET Standard é a padronização, não sendo um Framework, e sim uma Surface API.
    - Garante que tudo o que for escrito será compatível com ambos os frameworks.
- Sempre opte por versões LTS, para colocar as aplicações em produção.
- Runtime executa, SDK é utilizado para criar as aplicações .NET.

---

## .NET:

### Instalação

[Recurso adicional para instalação](https://balta.io/blog/dotnet-instalacao-configuracao-e-primeiros-passos)

Instalação:
- Acesse o link do [.NET](https://dotnet.microsoft.com/apps/aspnet).
- Clique em _Get Started_.
- Clique em _Download and Install_.
- Baixe o SDK - Software Development Kit, pois assim será possível desenvolver aplicações com .NET.
- Após a instalação do executável, basta seguir a ordem de execução do arquivo.

Verificando se o .NET foi instalado com sucesso no Windows:
- Abra um PowerShell.
- Execute o comando ``dotnet --version`` no PowerShell.
    - Se aparecer a versão do .NET no terminal, significa que tudo foi instalado corretamente.

### dotnet cli

CLI - Sigla para _Command Line Interface_.
- Interface de linha de comando.
- Comandos do CLI adicionais, integrados ao terminal.

Interfaces gráficas mudam constantemente, já interfaces via linha de comando não mudam com frequência.

Ao instalar o .NET do site oficial da Microsoft, foi instalado junto com uma **CLI**, o _dotnet CLI_.
- O dotnet CLI é definido pelo comando **_dotnet_**. Todo comando "dotnet ..." está executando o ``dotnet CLI``.
    - ``dotnet --version`` - Verifica a versão atual.
    - ``dotnet --list-sdks`` - Lista os SDKs instalados.
    - ``dotnet --list-runtimes`` - Lista os Runtimes instalados.
    - ``dotnet help`` - Exibe a ajuda, listando os comandos disponíveis.

**Dica**: [Configurando o Windows Terminal](https://balta.io/blog/windows-terminal)

### VS Code

Visual Studio Code - É um _Editor de Código_.

Visual Studio Community - É uma _IDE_ "Ambiente de Desenvolvimento Integrado". Uma IDE possui muito mais recursos do que um Editor de Código, sendo assim, é necessário uma máquina com melhor processamento para executar uma IDE com tranquilidade.

Instale o VS Code neste [link](https://code.visualstudio.com)

**Nota**: O comando ``code .`` no terminal, abre a pasta na qual você está acessando no momento no VS Code.

O VS Code é muito conhecido por suas extensões, que ajudam muito a produtividade no dia-a-dia.
- As extensões ficam disponíveis na barra lateral esquerda do VS Code.

Para esse curso introdutório, será necessário a extensão oficial "**C# - ``ms-dotnettools.csharp``** da Microsoft.

- O comando ``Ctrl + ,`` no VS Code, acessa as _Settings/Configurações_.
- O comando ``Ctrl + Shift + p`` Abre uma barra de pesquisa, com os comandos do VS Code, conhecida como **Show All Commands**.

### Tipos de projeto

O .NET é um framework para a criação de aplicações com as linguagens/ecossistema da Microsoft, permitindo assim a criação de projetos de vários tipos, como projetos web, websites, aplicações web, api, machine learning... Cada item/projeto/aplicação criada dentro do .NET, deve-se especificar o _tipo de projeto_ que será utilizado.

Cada _tipo de projeto_ gera um resultado final diferente.

Projeto do _tipo_ **Class Library** - Biblioteca de classe.
- O resultado final é uma DLL.
- Não possui interface.

Projeto do _tipo_ **Console Application**.
- O resultado final é uma aplicação que roda no terminal.
- Pode receber dados, esperar input do usuário.
- Possui resultados visíveis, através de uma interface.

Projeto **Web**.
- Projetos _Web_ no .NET são dividos em:
    - ASP.NET Web.
    - ASP.NET MVC.
    - ASP.NET WebAPI.

Projeto **Testes**.
- São do tipo _Microsoft Tests_.
- Projetos de Teste, para testar as aplicações antes de serem enviadas para os clientes, deixando assim, todos os testes _automatizados_.

Criando um novo projeto no .NET através do **dotnet cli**:
- Utiliza-se o ``dotnet new``:
    - ``dotnet new console`` => Novo _Console Application_.
    - ``dotnet new classlib`` => Novo _Class Library_.
    - ``dotnet new web`` => Novo projeto _ASP.NET Core_.
    - ``dotnet new mvc`` => Novo projeto _ASP.NET Core_.
    - ``dotnet new webapi`` => Novo projeto _ASP.NET Core_.
    - ``dotnet new mstest`` => Novo projeto _Microsoft Test_.
- Esses comandos criam as estruturas bases/iniciais da aplicação.

O comando ``dotnet new`` cria um projeto, sendo a mesma coisa que gerar os arquivos iniciais de uma aplicação. Esse comando sempre irá gerar os arquivos na pasta atual.
- Para especificar uma pasta, pode-se utilizar o "**-o**".
    - ``dotnet new console -o MeuApp``. Esse comando vai criar uma nova pasta chamada _MeuApp_ com os arquivos dentro.

**Dica**: As aplicações em .NET tendem a sempre começar com a primeira letra em Maiúscula do diretório.

### Fluxo de execução

Comandos principais do .NET:

``dotnet restore``
- Restaura todos os pacotes que a aplicação precisa para ser executada.
``dotnet build``
- Compila a aplicação.
``dotnet clean``
- Limpa as compilações anteriores e arquivos de cache.
``dotnet run``
- Compila e executa a aplicação.

**Dica**: Um projeto .NET deve ter um arquivo com extensão **csproj**, dentro do diretório raiz.

A primeira coisa a ser feita ao "pegar/abrir" uma aplicação .NET, é executar o comando ``dotnet restore`` para baixar todas as dependências/pacotes adicionais ao .NET Framework.

### Variáveis de ambiente

Variáveis de Ambiente:
- É comum ter vários ambientes para as aplicações.
    Exemplos:
    - Desenvolvimento.
        - Sua máquina é um ambiente de desenvolvimento.
    - Teste.
        - É um ambiente criado justamente para _testar_ as aplicações.
    - Homologação.
    - Produção.
    Esses ambientes se referem a onde a aplicação está rodando.
- Cada ambiente possui suas configurações - "variáveis de ambiente".
    - Chaves de acesso externo.
    - Conexões com bancos de dados.

**Dica**: Sempre procure ter um **ambiente de teste** para as aplicações.

Comando ``dotnet run``:
- No .NET é possível dizer qual ambiente se está utilizando.
    - dotnet run --environment=**$SEU_AMBIENTE**.
        - ``dotnet run --environment=development``.
        - ``dotnet run --environment=production``.
    - O comando _run_ não executa depuração (Debug).
        - Neste modo a aplicação não vai parar nos Break Points.

### Estrutura do App

Arquivo _.csproj_:
- Tem o Formato *XML*.
- Arquivo com definições do projeto.
- Está presente em todo projeto .NET

Arquivo _Program.cs_:
- Arquivo principal (C#).
- Porta de entrada.
- É o primeiro arquivo a ser executado.

**Nota**: A pasta _bin_ só aparece após a execução do comando ``dotnet build``. Sendo assim o resultado do build/compilação fica dentro da pasta _bin_, que se refere a **binário**.

_NomeDoArquivo_.csproj - O nome do arquivo _.csproj_, sempre seguirá o nome do projeto/app.
- **cs** - CSharp.
- **proj** - Projeto.
- ``<Project Sdk="Microsoft.NET.Sdk">``
    - Define que é uma estrutura de um projeto, e que esse projeto está utilizando o _.NET Sdk_.
- Seção/Grupo ``<PropertyGroup>`` dentro desse arquivo do projeto.
    - ``<OutputType>Exe<OutputType>`` - Tipo de saída _Console_ no .NET, com o Tipo **Exe**, ou seja, um executável.
    - ``<TargetFramework>netcoreapp3.1<TargetFramework>`` - Se refere a qual Framework essa aplicação está se baseando.

_Program.cs_ - Toda aplicação .NET, tem um ponto de entrada, como o _Program.cs_.
- Toda vez que é executado o comando ``dotnet run``, será buscado um arquivo **Program.cs** para ser executado.
- **Nota**: Nunca renomeie esse arquivo, sempre deixe o nome padrão.

A pasta _obj_, é utilizada para tempo de debbug da aplicação, ajudando a encontrar erros/bugs.

### Debug

Executando a aplicação em dois modos:
- Modo _Realese_ - Esse modo serve para **publicação** da aplicação.
    - Quando executado um ``dotnet run``, a aplicação é executada em _modo realese_ e nós desenvolvedores, somos os "clientes" que estão consumindo essa aplicação.

- Modo _debug/depuração_ - Modo utilizado para procurar/corrigir bugs/defeitos/falhas na aplicação.
    - Para realizar a _depuração_, é necessário abrir um arquivo com extensão **.cs**

**Dica**: Quando executado o comando ``dotnet run``, se não tiver nenhum **build**, será feito o _build_ automaticamente sem a necessidade do comando ``dotnet build``.

**Nota**: JSON - JavaScript Object Notation, é um formato de arquivo, assim como o XML. O JSON tem as definições do que é preciso ser executado na aplicação/programa.

### Revisão

Conteúdo do Módulo:
- Instalação simples e lado-a-lado.
    - Instalação do Sdk do .NET Core, Extensões, VSCode.
- Tipos de Projeto.
    - Projeto Web, Teste, Class Library, Console...
- Comandos Principais do .NET:
    - ``dotnet build``, ``dotnet run``, ``dotnet restore``.
- Ambientes de Produção, Desenvolvimento, Homologação...
- Como criar a estrutura de uma aplicação com C#.
- Como e o que é o Debug.

---

## Linguagem de Programação com C#:

### Notas importantes

Não deve ser utilizado _espaços e caracteres especiais_ na criação do programa.
    - Exemplos: **"MeuApp", "Pedidos", "MinhaApp"**, são bons nomes. Já os **"Meu App", "$App", "App #Teste"**, são nomes ruins que devem ser evitados.
Tente sempre utilizar caminhos curtos e sem caracteres especiais.
    - Bons: _c:\dev_, _C:\apps_.
    - Ruins: _C:\Caminho Com Espaços e Caracteres Especiais\Meu App_.
Evite criar aplicações em caminhos de rede.
    - Se possível sempre opte por utilizar o C:\
O C# é _Case Sensitive_.
    - Significa que diferencia maiúsculas de minúsculas.
        - **Teste** é diferente de **teste**.

### Escopo de um programa

### Namespaces

### Using

### Variáveis

### Constantes

### Palavras reservadas

### Comentários

### Tipos primitivos

### System

### Byte

### Números inteiros

### Números reais

### Boolean

### Char

### String

### Var

### Object

### Nullabel Types

### Alias

### Valores padrões

### Conversão implícita

### Conversão explícita

### Parse

### Convert

### Convertendo tipos

### Operadores aritméticos

### Operadores de atribuição

### Operadores de comparação

### Utilizando operadores

### Operadores lógicos

### Operador condicional: IF

### Utilizando IF

### Estrutura condicional: Switch

### Laços de repetição: For

### Laços de repetição: While

### Laços de repetição: Do/While

### Métodos e funções

### Métodos e funções: Prática

### Value Types e Reference Types

### Value Types e Reference Types: Prática

### Structs

### Structs: Prática

### Enums

### Revisão

---

## Mão na massa - Criando uma calculadora:

### Iniciando o projeto

### Soma

### Utilizando funções

### Subtração

### Divisão

### Multiplicação

### Menu da aplicação

### Chamando as funções

### Saindo da aplicação

### Revisão

---

## Mão na massa - Cronômetro:

### Iniciando o projeto

### Estrutura do cronômetro

### Thread e Sleep

### Criando o menu

### Opções do menu

### Substring

### Obtendo a opção

### Calculando o tempo

### Finalizando a aplicação

### Revisão

---

## Mão na massa - Editor de Textos:

### Iniciando o projeto

### Iteração e caractere de escape

### Do/While na prática

### StreamWriter

### Salvando o arquivo

### Abrindo arquivos

### Revisão

---

## Strings:

### Guids

### Interpolação de strings

### Comparação de strings

### StartsWith/EndsWith

### Equals

### Índices

### Métodos adicionais

### Manipulando strings

### StringBuilder

### Revisão

---

## Mão na massa - Editor HTML:

### Iniciando o projeto

### Desenhando a tela

### Exibindo o menu

### Menu da aplicação

### Editor

### Visualizador

### Substituindo caracteres

### Revisão

---

## Datas:

### Iniciando com datas

### Obtendo valores da data

### Formatando datas

### Padrões de formatação

### Adicionando valores

### Comparando datas

### CultureInfo

### Timezone

### Timespan

### Revisão

---

## Moedas:

### Tipo para moedas

### Formatando moedas

### Math

### Revisão

---

## Arrays:

### Arrays

### Percorrendo um array

### ForEach

### Alterando os valores

### Revisão

---

## Exceptions:

### Exceptions

### Try/Catch

### Tratando erros

### Disparando exceções

### Custom Exceptions

### Finally

### Revisão

---
