# TRABALHO-FACULDADE
TRABALHO FACULDADE CIÊNCIA DA COMPUTAÇÃO - COMPARAÇÃO DE CARTAS HARD-CODE
Esse foi um trabalho da faculdade com o objetivo de fazer comparação de cartas em C no modelo Hardcode, um trabalho simples porém com muitas aprendizagens, onde o principal conhecimento adquirido foi os atributos comparativos, já parou para pensar onde não temos que usar um sistema de comparações para acessarmos algum sistema? Desde talvez fazer um acesso a um sistema de login e senha até uma chave de acesso criptografada temos que usar um sistema de comparações podendo ser verdadeiro ou falso, ligado ou desligado, aberto ou fechado, etc. Usamos em várias situações um bom ponto de reflexão de sua real importancia e bem também interessante.



#include <stdio.h>
#include <string.h>
#include <strings.h> // Para strcasecmp()

int main() {
    char cidade_01[] = "Já-tem-pão";
    char cidade_02[] = "Rio-dos-peixinhos";

    int vitorias_carta01 = 0;
    int vitorias_carta02 = 0;

    // Comparação alfabética
    int resultado = strcasecmp(cidade_01, cidade_02);
    if (resultado == 0) {
        printf("As cidades têm o mesmo nome (ignorando maiúsculas/minúsculas).\n");
    } else if (resultado < 0) {
        printf("Carta 01 venceu alfabeticamente %s vem antes de %s.\n", cidade_01, cidade_02);
        vitorias_carta01++;
    } else {
        printf("Carta 02 venceu alfabeticamente %s vem depois de %s.\n", cidade_01, cidade_02);
        vitorias_carta02++;
    }

    // ESTADO DA CARTA
    int estado_da_carta01 = 00005;
    int estado_da_carta02 = 00004;
    if (estado_da_carta01 == estado_da_carta02) {
        printf("Empate, as cartas têm a mesma força.\n");
    } else if (estado_da_carta01 < estado_da_carta02) {
        printf("A carta 01 mais forte\n");
        vitorias_carta01++;
    } else {
        printf("A carta 02 mais forte\n");
        vitorias_carta02++;
    }

    // CÓDIGO DAS CARTAS
    int codigo_da_carta01 = 00005;
    int codigo_da_carta02 = 00005;
    if (codigo_da_carta01 == codigo_da_carta02) {
        printf("Empate, as cartas têm o mesmo código.\n");
    } else if (codigo_da_carta01 < codigo_da_carta02) {
        printf("A carta 01 venceu, tem um código maior\n");
        vitorias_carta01++;
    } else {
        printf("A carta 02 venceu, tem um código maior\n");
        vitorias_carta02++;
    }

    // POPULAÇÃO DAS CARTAS
    int populacao_carta_01 = 15000000;
    int populacao_carta_02 = 50000000;
    if (populacao_carta_01 < populacao_carta_02) {
        printf("A Carta 02 venceu, tem uma população maior\n");
        vitorias_carta02++;
    } else {
        printf("A Carta 01 venceu, tem uma população maior\n");
        vitorias_carta01++;
    }

    // ÁREA DA CARTA
    float area_carta_01 = 9.5;
    float area_carta_02 = 4.5;
    if (area_carta_01 > area_carta_02) {
        printf("A Carta 01 venceu, tem a maior área\n");
        vitorias_carta01++;
    } else {
        printf("A Carta 02 venceu, tem a maior área\n");
        vitorias_carta02++;
    }

    // PIB DA CARTA
    int pib_carta_01 = 500000;
    int pib_carta_02 = 1000000;
    if (pib_carta_01 < pib_carta_02) {
        printf("A Carta 02 venceu, tem o maior PIB\n");
        vitorias_carta02++;
    } else {
        printf("A Carta 01 venceu, tem o maior PIB\n");
        vitorias_carta01++;
    }

    // NÚMEROS DE PONTOS TURISTICOS DA CARTA
    int numeros_de_pontos_turisticos_carta_01 = 5;
    int numeros_de_pontos_turisticos_carta_02 = 15;
    if (numeros_de_pontos_turisticos_carta_01 > numeros_de_pontos_turisticos_carta_02) {
        printf("A Carta 01 venceu, tem mais pontos turísticos\n");
        vitorias_carta01++;
    } else {
        printf("A Carta 02 venceu, tem mais pontos turísticos\n");
        vitorias_carta02++;
    }

    // Calcular Densidade Populacional e PIB per capita
    printf("\n=== DADOS ADICIONAIS ===\n");

    // Densidade Populacional: População / Área
    float densidade_populacional_carta_01 = populacao_carta_01 / area_carta_01;
    float densidade_populacional_carta_02 = populacao_carta_02 / area_carta_02;
    printf("Densidade populacional Carta 01: %.2f hab/km²\n", densidade_populacional_carta_01);
    printf("Densidade populacional Carta 02: %.2f hab/km²\n", densidade_populacional_carta_02);

    // PIB per capita: PIB / População
    float pib_per_capita_carta_01 = (float)pib_carta_01 / populacao_carta_01;
    float pib_per_capita_carta_02 = (float)pib_carta_02 / populacao_carta_02;
    printf("PIB per capita Carta 01: R$ %.2f\n", pib_per_capita_carta_01);
    printf("PIB per capita Carta 02: R$ %.2f\n", pib_per_capita_carta_02);


  // CONTAGEM DE VITÓRIAS
  printf("\n=== TOTAL DE VITÓRIAS ===\n");
  printf("Carta 01 (%s): %d vitórias\n", cidade_01, vitorias_carta01);
  printf("Carta 02 (%s): %d vitórias\n", cidade_02, vitorias_carta02);

  if (vitorias_carta01 > vitorias_carta02) {
      printf("\nA carta vencedora foi: %s com %d vitórias!\n", cidade_01, vitorias_carta01);
  } else if (vitorias_carta02 > vitorias_carta01) {
      printf("\nA carta vencedora foi: %s com %d vitórias!\n", cidade_02, vitorias_carta02);
  } else {
      printf("\nEMPATE! Ambas as cartas tiveram %d vitórias.\n", vitorias_carta01);
  }


  

    return 0;
}


// OI PROFESSOR TUDO BEM? QUERO AGRADECER PELAS AULAS NÃO SEI SE VOCÊ VAI VER ESSE CÓDIGO POIS SÃO MUUTOS ALUNOS VOU CONFESSAR QUE USEI UM POUCO DE IA SOMENTE PARA DAR UMA INCREMENTADA PORÉM SE VOCÊ VER EU VOU AGRADECER MUITO, SE VOCÊ ME SEGUIR AQUI DO GITHUB EU SIGO VC DE VOLTA  :) E SERÁ UM DOS MOTIVOS PARA EU NÃO DESISTIR DO CURSO PORÉM VAMOS SEGUIR FORTES!!!!!!
