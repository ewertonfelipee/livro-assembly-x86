---
description: Livro gratuito sobre Assembly x86 e x86-64
---

# Introdução

Este livro é mais um projeto do [Mente Binária](https://mentebinaria.com.br) cujo o intuito é ensinar os fundamentos do Assembly x86 e x86-64. Nele será abordado desde o zero até conceitos mais avançados afim de dar um entendimento profundo e uma base sólida de conhecimento.

O Mente Binária também tem um livro sobre [Fundamentos de Engenharia Reversa](https://mentebinaria.gitbook.io/engenharia-reversa/) e diversos [treinamentos gratuitos](https://www.mentebinaria.com.br/treinamentos/).

{% hint style="info" %}
Se você está lendo isto no [repositório do GitHub](https://github.com/Silva97/livro-assembly-x86), recomendo que leia na plataforma do GitBook [clicando aqui](https://mentebinaria.gitbook.io/assembly-x86/).
{% endhint %}

## Por que aprender Assembly?

Se você quer aprender Assembly achando que vai conseguir fazer programas mais rápidos diretamente em Assembly, saiba que está (quase) enganado. Os algoritmos de otimização dos compiladores de hoje em dia tem uma eficiência impressionante a ponto de superar as habilidades humanas. Ou seja é muito mais eficiente escrever um código em C, por exemplo, do que diretamente em Assembly. Claro que ainda é possível fazer código mais eficiente diretamente em Assembly porém apenas em casos específicos e se você tiver bastante experiência. Ou seja é mais interessante usar Assembly em conjunto com C do que fazer todo o software em Assembly.

Apesar disso aprender Assembly nos dias atuais tem sim utilidade e irei listar algumas:

1. Engenharia Reversa (de software)\
   Entender como um software funciona na prática só é de fato possível se você souber Assembly. Usar [_decompiler_](https://pt.wikipedia.org/wiki/Descompilador) até funciona em parte mas não pense que isso tem grandes utilidades o tempo todo.
2. Exploração de binários\
   Para quem quer fazer testes de segurança em binários, Assembly é indispensável.
3. Otimização de código\
   Sim, como eu já disse é mais eficiente não escrever o código diretamente em Assembly. Porém saber Assembly e usar esse conhecimento para estudar o código de saída de um compilador de uma determinada linguagem (GCC por exemplo) vai te fazer aprender muita coisa sobre o código resultante. Esse conhecimento vai te ajudar e muito a fazer códigos mais eficientes nesta linguagem. Isto é claro, é especialmente útil em linguagens que te permitem prever o código de saída (volto a repetir C como exemplo).
4. Otimização de código²\
   Também dá para fazer otimizações de código para processadores específicos manualmente. Podemos ver vários exemplos desta façanha no famigerado ffmpeg. [Veja aqui](https://github.com/FFmpeg/FFmpeg/blob/a0ac49e38ee1d1011c394d7be67d0f08b2281526/libavcodec/x86/ac3dsp.asm).
5. Tarefas de "baixo nível"\
   Algumas instruções específicas de determinados processadores são basicamente impossíveis de serem utilizadas em uma linguagem de alto nível. Uma tarefa básica em Assembly, como chamar uma [interrupção de software](https://pt.wikipedia.org/wiki/Interrup%C3%A7%C3%A3o), é impossível de ser feita em uma linguagem de alto nível como C.
6. C & Assembly\
   Termino falando que há uma incrível vantagem de se saber Assembly quando se programa em C. Não só pelo [inline Assembly](https://gcc.gnu.org/onlinedocs/gcc/Using-Assembly-Language-with-C.html) mas também pela previsibilidade do código que eu já mencionei (você vai entender o que é isso se continuar lendo o livro).

Como podemos ver o conhecimento da linguagem Assembly nos dias atuais é, na maioria dos casos, mais útil do que programar nela diretamente.

## O que é Assembly?

De forma resumida Assembly é uma notação em formato de texto das instruções do código de máquina de uma determinada arquitetura. A "arquitetura" ao qual me refiro aqui é o ISA (_Instruction Set Architecture_) onde ela cria um modelo abstrato de um computador e tem diversas instruções que são computadas pelo processador, essas instruções são o que é conhecido como código de máquina.

Falando de um ponto de vista humano entender instruções em código de máquina é uma tarefa árdua. Por isso os manuais do ISA costumam simplificar o entendimento da instrução se referindo a ela com uma notação em texto, onde essa notação é conhecida como mnemônico e tem o fim de facilitar o entendimento e a memorização da instrução do processador.

E é justamente dessa notação em texto dos manuais que surgiu o que a gente conhece hoje como "linguagem Assembly". Onde na verdade não existe uma linguagem Assembly (ou ASM para abreviar) mas sim cada ISA tem uma linguagem ASM diferente.

Os programadores antigamente escreviam o código usando a notação em texto (Assembly) e depois, a partir dela, convertiam para código de máquina manualmente. Mas felizmente hoje em dia existem softwares que fazem essa conversão de maneira automática e eles são chamados de **assemblers**.

{% hint style="info" %}
Apesar de eu estar utilizando letra maiúscula para escrever a palavra "Assembly" ela na verdade não é um substantivo próprio mas sim a palavra "montagem" em inglês. Estou fazendo isso meramente por uma estilização pessoal.
{% endhint %}

## O que é assembler?

O assembler é um compilador que converte código em Assembly para o código de máquina. Muito antigamente, nos primórdios da computação, uma pessoa manualmente convertia os códigos em Assembly para código de máquina. Depois inventaram uma máquina para automatizar essa tarefa sendo chamada de "assembler". Nos dias atuais o "assembler" é um software de computador.

{% hint style="warning" %}
É muito comum as pessoas se confundirem e dizerem "linguagem _assembler_", o que está errado. Cuidado para não se confundir também.
{% endhint %}

## O autor

Meu nome é Luiz Felipe. Pronto, agora você sabe tudo sobre mim.

[GitHub](https://github.com/Silva97) | [Facebook](https://www.facebook.com/B4.0E.B0.48.CD.10.B0.69.CD.10.C3) | [Twitter](https://twitter.com/Vilas\_79) | [Medium](https://freedev.medium.com) | [Perfil no Mente Binária](https://www.mentebinaria.com.br/profile/522-felipesilva/)

## Licença

Este conteúdo está sendo compartilhado sobre os termos da licença [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/legalcode). Essa licença permite que você compartilhe o conteúdo, mesmo que para fins lucrativos, desde que seja compartilhado sob os termos da mesma licença e sem adicionar novas restrições. Como também é necessário que dê os créditos pelo trabalho original.

Para mais detalhes sobre a licença consulte o link abaixo:

* [Atribuição-CompartilhaIgual 3.0 Não Adaptada (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/deed.pt)
