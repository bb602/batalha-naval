<p align="center">
  <img src="https://github.com/felipemfp/batalha-naval/blob/gh-pages/images/favicon.png" />
</p>

# Batalha Naval

Batalha naval é um jogo de tabuleiro de dois jogadores, no qual os jogadores têm de adivinhar em que quadrados estão os navios do oponente. Embora o primeiro jogo em tabuleiro comercializado e publicado pela Milton Bradley Company em 1931, o jogo foi originalmente jogado com lápis e papel. Seu objectivo é derrubar os barcos do oponente adversário,ganha quem derrubar todos os navios adversários primeiro.¹

¹ [Batalha Naval - Wikipedia](https://pt.wikipedia.org/wiki/Batalha_naval_(jogo))
      

Preparação: Cada jogador recebe dois tabuleiros: um para posicionar seus navios e outro para registrar os tiros do oponente. 
Posicionamento: Os navios são posicionados em seus respectivos tabuleiros, sem que o oponente veja a posição deles. 
Jogada: Os jogadores alternam atirando no tabuleiro do oponente, informando as coordenadas (linha e coluna) do tiro. 
Aviso: O oponente responde se o tiro foi no navio ou na água. 
Afundar: Um navio é considerado afundado quando todas as suas posições são acertadas. 
Fim do jogo: O jogo termina quando um dos jogadores afunda todos os navios do oponente. 



Requisitos em C:
Para implementar o Batalha Naval em C, você precisará de algumas estruturas e funções:
Tabuleiros:
Representar os tabuleiros usando matrizes bidimensionais (arrays de arrays). 
Navios:
Definir a estrutura para cada navio (tamanho, posição, estado (afundado ou não)). 
Disparos:
Implementar a função para processar um disparo, verificar se acertou um navio e atualizar os tabuleiros. 
Verificação de vitória:
Função para verificar se um jogador ganhou (todos os navios do oponente afundados). 
Interface com o usuário:
Funções para exibir os tabuleiros, receber as coordenadas do tiro e mostrar mensagens. 

#include <stdio.h>
#include <stdlib.h>

#define TAMANHO_TABULEIRO 10 // Defina o tamanho do tabuleiro

// Estrutura para representar um navio
typedef struct {
    int tamanho;
    int posicoes[TAMANHO_TABULEIRO * TAMANHO_TABULEIRO]; // Armazena as posições do navio
    int afundado; // 0 - não afundado, 1 - afundado
} Navio;

// Estrutura para representar um jogador
typedef struct {
    char tabuleiro[TAMANHO_TABULEIRO][TAMANHO_TABULEIRO]; // Tabuleiro do jogador (água = '.', navio = '#', tiro = 'X')
    Navio navios[5]; // Array de navios (ex: 1 porta-aviões, 1 navio-mãe, 2 cruzadores, 1 submarino)
} Jogador;

int main() {
    Jogador jogador1, jogador2;

    // Inicializar os tabuleiros (tudo com água - '.')
    for (int i = 0; i < TAMANHO_TABULEIRO; i++) {
        for (int j = 0; j < TAMANHO_TABULEIRO; j++) {
            jogador1.tabuleiro[i][j] = '.';
            jogador2.tabuleiro[i][j] = '.';
        }
    }

    // Posicionar os navios (exemplo, você pode implementar a lógica para o usuário escolher)
    // ... [Lógica para posicionamento] ...

    // Loop principal do jogo
    while (1) { // Jogo continua até que um jogador ganhe
        // Jogada do jogador 1
        // ... [Lógica para receber as coordenadas do tiro, verificar se acertou, etc.] ...

        // Jogada do jogador 2
        // ... [Lógica para receber as coordenadas do tiro, verificar se acertou, etc.] ...

        // Verificar se algum jogador ganhou
        // ... [Lógica para verificar se algum jogador afundou todos os navios do oponente] ...
        // Se algum jogador ganhou, break do loop e mensagem de fim de jogo

    }

    return 0;
}
