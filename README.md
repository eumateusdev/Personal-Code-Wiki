# Seja bem vindo a minha wikipedia pessoal de códigos. 


<p align="center">
⚠️ Projeto  em constante atualização ⚠️
</p>

<p align="justify">
Esta wikipedia é uma jornada pessoal, fruto de incontáveis horas de dedicação e paixão pela arte da programação. Desde os primeiros passos em linhas de código até os desafios mais complexos, compartilho aqui um pouco de mim e do meu aprendizado ao longo do tempo.

Para cada linguagem esta wiki documenta as bibliotecas e funções que foram utilizas durante o ensino.
</p>

# índice

# 👨‍💻 C++
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

A biblioteca iostream (input/output stream) é uma parte fundamental da linguagem C++, permitindo a interação com a entrada (teclado) e saída (tela) do programa. Com ela, você pode realizar operações de leitura e escrita em tempo de execução. Exemplo:

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



