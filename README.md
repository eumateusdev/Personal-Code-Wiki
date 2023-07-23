# Seja bem vindo a minha wikipedia pessoal de códigos. 


<p align="center">
⚠️ Projeto  em constante atualização ⚠️
</p>

<p align="justify">
Esta wikipedia é uma jornada pessoal, fruto de incontáveis horas de dedicação e paixão pela arte da programação. Desde os primeiros passos em linhas de código até os desafios mais complexos, compartilho aqui um pouco de mim e do meu aprendizado ao longo do tempo.

Para cada linguagem esta wiki documenta as bibliotecas e funções que foram utilizas durante o ensino.
</p>

# índice

# 👨‍💻 [C++](#-c-1)
- [Sobre a linguagem](#sobre-a-linguagem)
- [Bibliotecas](#bibliotecas)
  - [iostream](#iostream)
  - [string](#string)
  - [map](#map)
  - [vector](#vector)
  - [fstream](#fstream)
  - [ctime](#ctime)
  - [cstdlib](#cstdlib)
- [Funções](#funções)
  - [main](#main)
  - [cin e cout](#cin-e-cout)
  - [open](#open)
  - [close](#close)
  - [push_back](#push_back)
  - [srand](#srand)
  - [rand](#rand)
  - [exit](#exit)
- [Organização](#organização)
  - [Qual a real utilidade de arquivos de cabeçalho?](#qual-a-real-utilidade-de-arquivos-de-cabeçalho)
  - [Como utilizar a mesma variável em múltiplos arquivos?](#como-utilizar-a-mesma-variável-em-múltiplos-arquivos)

## 👨‍💻 C++
## Sobre a linguagem

<p align="justify">
C++ é uma linguagem de programação de uso geral que foi desenvolvida como uma extensão da linguagem C, permitindo que os programadores utilizem os recursos do C e adicionem recursos de programação orientada a objetos (POO). Criada por Bjarne Stroustrup, C++ foi lançada pela primeira vez em 1985 e desde então tem sido amplamente utilizada em diversas aplicações, incluindo sistemas operacionais, jogos, aplicações desktop, aplicações web, dispositivos embarcados, entre outros.

- Programação Orientada a Objetos (POO): C++ suporta a POO, permitindo aos desenvolvedores criar classes e objetos que encapsulam dados e comportamentos relacionados. Isso facilita a organização do código e promove a reutilização de código, tornando-o mais modular e fácil de manter.

- Eficiência e Desempenho: C++ foi projetado com um foco na eficiência e desempenho. Ele oferece um controle próximo do hardware, permitindo aos programadores otimizar o código para obter melhor performance. Isso torna a linguagem popular para desenvolvimento de sistemas que requerem alto desempenho e baixo consumo de recursos.

- Polimorfismo: C++ suporta polimorfismo, permitindo que as classes derivadas possam ser tratadas como objetos da classe base. Isso facilita a criação de hierarquias de classes e a implementação de herança.

- Templates: Os templates em C++ são uma poderosa ferramenta que permitem a criação de código genérico, o que resulta em maior reutilização de código e flexibilidade na criação de estruturas de dados e algoritmos.

- Gerenciamento de memória: C++ permite o gerenciamento manual de memória, através de ponteiros, mas também oferece recursos de gerenciamento automático de memória por meio do uso de classes como "smart pointers" e "contêineres STL" (Standard Template Library).

- Multi-paradigma: Além de ser uma linguagem orientada a objetos, C++ também suporta programação procedural e programação genérica. Isso significa que os desenvolvedores têm a flexibilidade de escolher o paradigma de programação que melhor se adapta ao problema em questão.

- Biblioteca Padrão: C++ possui uma extensa biblioteca padrão, conhecida como Standard Template Library (STL), que fornece uma ampla gama de funcionalidades e estruturas de dados prontas para uso, tornando o desenvolvimento mais rápido e eficiente.

</p>

## Bibliotecas
<p align="justify">
A linguagem de programação C++ é amplamente utilizada e possui diversas bibliotecas que oferecem funcionalidades poderosas para a manipulação de dados, entrada/saída, manipulação de strings e muito mais. Abaixo estão as bibliotecas utilizadas nos projetos presentes neste repositório:


- ### iostream

A biblioteca iostream (input/output stream) é uma parte fundamental da linguagem C++, permitindo a interação com a entrada (teclado) e saída (tela) do programa. Com ela, pode-se realizar operações de leitura e escrita em tempo de execução. Exemplo:

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Digite um número: ";
    cin >> number;
    cout << "Você digitou: " << number << endl;
    return 0;
}
```
- ### string

A biblioteca string fornece recursos para manipular sequências de caracteres. Ela permite criar, comparar, concatenar e extrair substrings de strings. Exemplo:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string nome = "Alice";
    cout << "O tamanho da string é: " << nome.length() << endl;
    return 0;
}

```

- ### map

A biblioteca map implementa um contêiner de mapeamento associativo, também conhecido como tabela de hash, em que os dados são armazenados em pares chave-valor. É uma estrutura muito útil para armazenar e recuperar dados de forma eficiente. Exemplo:

```cpp
#include <iostream>
#include <map>
using namespace std;

int main() {
    map<string, int> idadePorNome;
    idadePorNome["Alice"] = 30;
    idadePorNome["Bob"] = 25;

    cout << "A idade de Alice é: " << idadePorNome["Alice"] << endl;
    return 0;
}
```

- ### vector

A biblioteca vector é uma implementação de array dinâmico que permite armazenar uma coleção de elementos em sequência. É muito útil quando o número de elementos não é conhecido antecipadamente ou pode mudar ao longo do tempo. Exemplo:

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> numeros;
    numeros.push_back(10);
    numeros.push_back(20);
    numeros.push_back(30);

    for (int numero : numeros) {
        cout << numero << " ";
    }
    cout << endl;
    return 0;
}
```

- ### fstream

A biblioteca fstream (file stream) fornece classes para a manipulação de arquivos. Ela permite ler e escrever dados em arquivos de texto ou binários. Exemplo:

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream arquivo("meuarquivo.txt");
    if (arquivo.is_open()) {
        arquivo << "Este é um exemplo de escrita em arquivo usando C++." << endl;
        arquivo.close();
    } else {
        cout << "Não foi possível abrir o arquivo." << endl;
    }
    return 0;
}
```

- ### ctime

A biblioteca ctime fornece funções relacionadas ao tempo e data. É útil para obter informações sobre a data e hora atual ou para manipular e formatar valores de data e hora. Exemplo:

```cpp
#include <iostream>
#include <ctime>
using namespace std;

int main() {
    time_t agora = time(nullptr);
    cout << "A data e hora atual é: " << ctime(&agora);
    return 0;
}
```

- ## cstdlib

A biblioteca cstdlib fornece funções para manipulação de memória e outras operações de sistema. É comumente usada para a geração de números aleatórios, alocação dinâmica de memória, controle de fluxo do programa e outras tarefas de baixo nível. Exemplo:

```cpp
#include <iostream>
#include <cstdlib>
using namespace std;

int main() {
    int numeroAleatorio = rand() % 100;
    cout << "Número aleatório entre 0 e 99: " << numeroAleatorio << endl;
    return 0;
}
```
</p>

## Funções

<p align="justify">

- ## main

Essa é a função principal do programa. É onde a execução do programa começa. A função main() chama outras funções para executar.

```cpp
#include <iostream>

// Função principal do programa
int main() {
    // Código
    // ...
    return 0;
}
```

- ## cin e cout

São objetos da biblioteca iostream utilizados para realizar a entrada (comando cin) e saída (comando cout) de dados no console. Eles permitem que o programa interaja com o usuário, lendo informações do teclado (cin) e exibindo mensagens e resultados na tela (cout).

```cpp
#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Digite um número: ";
    cin >> numero;
    cout << "Você digitou: " << numero << endl;
    return 0;
}
```

- ## open

É um método da classe ifstream (input file stream) que abre um arquivo para leitura. A classe ifstream faz parte da biblioteca fstream, que é usada para manipulação de arquivos. Através do método open(), é possível abrir um arquivo de texto ou binário para leitura e acessar seu conteúdo.

```cpp
#include <fstream>
#include <iostream>
using namespace std;

int main() {
    ifstream arquivo("meuarquivo.txt");
    if (arquivo.is_open()) {
        // Arquivo foi aberto com sucesso, faça a leitura dos dados
    } else {
        cout << "Não foi possível abrir o arquivo." << endl;
    }
    arquivo.close();
    return 0;
}
```

- ## close

É um método da classe ifstream (input file stream) que fecha o arquivo após a leitura. O método close() é usado para encerrar o acesso ao arquivo após a leitura dos dados necessários. Isso libera os recursos associados ao arquivo e previne erros de manipulação.

```cpp
#include <fstream>
#include <iostream>
using namespace std;

int main() {
    ifstream arquivo("meuarquivo.txt");
    if (arquivo.is_open()) {
        // Faça a leitura dos dados no arquivo
        arquivo.close(); // Fecha o arquivo após a leitura
    }
    return 0;
}
```

- ## push_back

É um método da classe vector que adiciona um elemento no final do vetor. A classe vector é parte da biblioteca vector e implementa um array dinâmico que pode crescer automaticamente conforme novos elementos são adicionados. O método push_back() é utilizado para inserir um novo elemento no final do vetor.

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> numeros;
    numeros.push_back(10);
    numeros.push_back(20);
    numeros.push_back(30);

    for (int numero : numeros) {
        cout << numero << " ";
    }
    cout << endl;
    return 0;
}
```

- ## srand

É uma função da biblioteca cstdlib que inicializa a semente do gerador de números aleatórios. O gerador de números aleatórios utiliza uma "semente" como ponto de partida para a geração de números. Ao chamar a função srand(), podemos definir a semente manualmente para obter sequências diferentes de números aleatórios em diferentes execuções do programa.

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    // Inicializa a semente do gerador de números aleatórios com o valor do horário atual
    srand(time(nullptr));

    // Gera um número aleatório entre 0 e 99
    int numeroAleatorio = rand() % 100;
    cout << "Número aleatório entre 0 e 99: " << numeroAleatorio << endl;

    return 0;
}
```

- ## rand

É uma função da biblioteca cstdlib que gera um número inteiro aleatório. A função rand() retorna um número inteiro aleatório dentro de um intervalo específico, que pode ser manipulado usando operações matemáticas.

```cpp
#include <iostream>
#include <cstdlib>
using namespace std;

int main() {
    // Gera um número aleatório entre 0 e RAND_MAX
    int numeroAleatorio = rand();
    cout << "Número aleatório: " << numeroAleatorio << endl;

    return 0;
}
```

- ## exit

É uma função da biblioteca cstdlib que termina o programa imediatamente. Ao chamar a função exit(), o programa é encerrado imediatamente, sem executar o restante do código ou realizar qualquer limpeza de recursos. É comum usar exit() para terminar o programa em casos de erros ou situações de emergência.

```cpp
#include <cstdlib>
#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Digite um número: ";
    cin >> numero;

    if (numero < 0) {
        cout << "Número inválido. O programa será encerrado." << endl;
        exit(1); // Termina o programa imediatamente com código de erro 1
    }

    cout << "Número digitado: " << numero << endl;

    return 0;
}
```

</p>

## Organização

<p align="justify">
Em projetos de programação em C++, é comum dividir o código em vários arquivos para melhor organização, modularidade e reutilização de código. Essa abordagem é conhecida como "separação de código em múltiplos arquivos" ou "organização em arquivos".

Aqui está um exemplo de como organizar um projeto simples em C++ com três arquivos: main.cpp, funcoes.h e funcoes.cpp.

- main.cpp: Este é o arquivo principal onde chamará as funções definidas nos outros arquivos.

```cpp
#include "funcoes.h"
#include <iostream>
using namespace std;

int main() {
    int a = 5, b = 10;
    int resultado = somar(a, b);
    cout << "A soma de " << a << " e " << b << " é: " << resultado << endl;
    return 0;
}
```

- funcoes.h: Este é o arquivo de cabeçalho (header file) que contém as declarações das funções que serão utilizadas em outros arquivos.

```cpp
int somar(int a, int b);
```

- funcoes.cpp: Este é o arquivo de implementação que contém o código das funções declaradas no arquivo funcoes.h.

```cpp
#include "funcoes.h"

int somar(int a, int b) {
    return a + b;
}
```

### Qual a real utilidade de arquivos de cabeçalho?
Os arquivos de cabeçalho (header files) em C++ têm uma utilidade essencial na organização do código e são usados para declarar interfaces das funções, classes e outras estruturas que serão utilizadas em outros arquivos-fonte (.cpp).

Aqui estão algumas razões pelas quais os arquivos de cabeçalho são úteis:

- Declaração de Interfaces: Os arquivos de cabeçalho contêm apenas as declarações das funções e classes, sem a implementação. Isso permite que outros arquivos saibam quais funções e classes estão disponíveis para uso, sem precisar conhecer os detalhes de como elas funcionam.

- Evitar Redefinição: Quando é incluido um arquivo de cabeçalho em vários arquivos-fonte, o pré-processador do C++ garante que as definições sejam incluídas apenas uma vez em cada unidade de compilação, evitando assim erros de redefinição.

- Reutilização de Código: Ao dividir o código em arquivos de cabeçalho e arquivos de implementação, pode-se reutilizar as mesmas declarações em diferentes partes do projeto, facilitando a manutenção e evitando a duplicação de código.

### Como utilizar a mesma variável em múltiplos arquivos?

Para utilizar a mesma variável em múltiplos arquivos, deve seguir as seguintes etapas:

- Declaração da variável no arquivo de cabeçalho: Declare a variável no arquivo de cabeçalho para torná-la conhecida em todos os arquivos que incluem esse cabeçalho. Use a palavra-chave extern para indicar que a variável está sendo declarada, mas não definida nesse arquivo.

```cpp
extern int variavelGlobal;
```
- Definição da variável em um arquivo-fonte: Em um arquivo-fonte (.cpp) específico, defina a variável global que foi declarada no arquivo de cabeçalho.

```cpp
#include "arquivo_global.h"

int variavelGlobal = 42;
```

- Inclusão do arquivo de cabeçalho em outros arquivos-fonte: Agora, é possivél usar a variável global em outros arquivos-fonte, incluindo o arquivo de cabeçalho onde a variável foi declarada.

```cpp
// outro_arquivo.cpp
#include "arquivo_global.h"
#include <iostream>

int main() {
    std::cout << "Valor da variável global: " << variavelGlobal << std::endl;
    return 0;
}
```

</p>

## Funções Inline

<p align="justify">

Em C++, funções inline são pequenas funções que são incorporadas diretamente no código onde são chamadas, em vez de serem executadas através de uma chamada de função convencional. A ideia é otimizar o desempenho evitando o overhead de empilhar e desempilhar valores da pilha de chamadas de função.

Para declarar uma função inline em C++, pode-se usar a palavra-chave inline antes da definição da função. Normalmente, funções inline são colocadas no cabeçalho (arquivo .h) para que possam ser acessadas em diferentes arquivos de origem (arquivos .cpp).

Exemplo de função inline em C++:

```cpp
// arquivo: funcoes_inline.h

// Função inline para calcular o quadrado de um número
inline int quadrado(int num) {
    return num * num;
}
```

```cpp
// arquivo: main.cpp
#include <iostream>
#include "funcoes_inline.hpp" // Incluindo o cabeçalho com a função inline

int main() {
    int num = 5;

    // Chamando a função inline para calcular o quadrado do número
    int resultado = quadrado(num);

    std::cout << "O quadrado de " << num << " é: " << resultado << std::endl;
    return 0;
}

```

No exemplo acima, a função quadrado foi declarada como inline no cabeçalho funcoes_inline.hpp e definida logo em seguida. Em seguida, no arquivo main.cpp, a função quadrado é chamada normalmente, como se fosse uma função regular, mas o compilador pode optar por substituir a chamada da função pelo próprio corpo da função, inlineando-a diretamente no código onde foi chamada.

É importante notar que o compilador tem a liberdade de decidir se realmente irá tratar uma função como inline ou não. A palavra-chave inline é apenas uma sugestão ao compilador. Além disso, é recomendado usar funções inline apenas para funções pequenas e simples, pois funções mais complexas podem resultar em um código maior e, potencialmente, reduzir o desempenho em vez de melhorá-lo.
</p>

