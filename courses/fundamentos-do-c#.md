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

### .NET Standard

### .NET 5

### LTS

### Versionamento

### Runtime e SDK

### Revisão

---

## .NET:

### Instalação

### dotnet cli

### VS Code

### Tipos de projeto

### Fluxo de execução

### Variáveis de ambiente

### Estrutura do App

### Debug

### Revisão

---

## Linguagem de Programação com C#:

### Notas importantes

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
