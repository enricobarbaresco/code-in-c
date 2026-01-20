# Variáveis e Tipos de Dados

Variáveis são espaços na memória usados para armazenar valores.

Na linguagem C, todo valor precisa ter um tipo definido, como:
- int (inteiro)
- float (decimal)
- char (caractere)

Definir corretamente os tipos ajuda a evitar erros e torna o programa mais eficiente.

**printf()** é usado para exibir informações na tela. **scanf()** é usado para ler dados que o usuário digita.

Esses são os comandos mais básicos de comunicação com o usuário!

**Especificadores de formato principais:**
- %d → Inteiro decimal
- %f → Número de ponto flutuante (float)
- %lf → Número de ponto flutuante duplo (double)
- %c → Caractere único
- %s → String (texto)
- %x → Hexadecimal
- %o → Octal
- %% → Imprime o símbolo %

EXEMPLO DE CÓDIGO:

#include <stdio.h>

int main() {
    int idade;
    char nome[50];
    
    printf("Digite seu nome: ");
    scanf("%s", nome);  // String não precisa de &
    
    printf("Digite sua idade: ");
    scanf("%d", &idade);
    
    printf("Olá, %s! Você tem %d anos!\n", nome, idade);
    
    return 0;
}

Explicação linha por linha:
→
int idade; → Declara uma variável para guardar um número inteiro
→
char nome[50]; → Declara um array de caracteres (string) com espaço para 50 caracteres
→
printf("Digite sua idade: "); → Exibe uma mensagem pedindo a idade
→
scanf("%d", &idade); → Lê um número inteiro e guarda em 'idade'
→
%d → Formato para números inteiros
→
&idade → O & indica o endereço da variável (onde guardar o valor)
→
scanf("%s", nome); → Para strings, não usamos & pois o nome do array já é um endereço
