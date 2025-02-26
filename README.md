# seven-days-of-code 👩🏽‍💻

**#7DaysOfCode - Lógica JS 1/7: Operações Booleanas**

Este primeiro dia é super importante! Ao final dele, você terá um novo conhecimento que é essencial para os próximos desafios.

Existe uma situação super comum para quem utiliza o Javascript: problemas com os tipos de variáveis na hora de comparar os valores de duas variáveis entre si. Eu já passei muito por isso!

Em linguagens de programação compiladas, como Java e C#, esse problema é detectado em tempo de compilação, e você que está desenvolvendo o código tem um aviso claro do erro.

Já no Javascript, esses erros passam despercebidos, já que o código não passa por um compilador. Ou seja, os erros só aparecem em tempo de execução.

A parte mais confusa para quem está começando a aprender lógica com Javascript é a operação de igualdade entre valores. Dependendo de como você escrever o seu código, o Javascript fará uma conversão de tipo para um tipo booleano de maneira implícita (automática), e isso afetará variáveis que eram Strings, Numbers, Object, etc….

Isso causa alguns comportamentos estranhos, como todos esses exemplos aqui abaixo retornando true:
````javascript
console.log( false == '0' );
console.log( null == undefined );
console.log( " \t\r\n" == 0 );
console.log( ' ' == 0 );
````

O que não faz necessariamente muito sentido.

(Você pode testar tudo isso indo no seu navegador, clicando com o botão direito, escolhendo a opção “Inspecionar” e a aba “Console”. Nessa aba, basta copiar e colar cada uma das linhas acima para confirmar que todas realmente retornam true).

Sendo assim, a sua tarefa de hoje é reescrever o código abaixo de maneira que ele imprima as informações de maneira correta, que faça sentido e sem erros:

````javascript
let numeroUm = 1
let stringUm = '1'
let numeroTrinta = 30
let stringTrinta = '30'
let numeroDez = 10
let stringDez = '10'

if (COMPARAR O numeroUm e a stringUm) {
  console.log('As variáveis numeroUm e stringUm tem o mesmo valor, mas tipos diferentes')
} else {
  console.log('As variáveis numeroUm e stringUm não tem o mesmo valor')
}

if (COMPARAR O numeroTrinta e a stringTrinta) {
  console.log('As variáveis numeroTrinta e stringTrinta tem o mesmo valor e mesmo tipo')
} else {
  console.log('As variáveis numeroTrinta e stringTrinta não tem o mesmo tipo')
}

if (COMPARAR O numeroDez e a stringDez) {
  console.log('As variáveis numeroDez e stringDez tem o mesmo valor, mas tipos diferentes')
} else {
  console.log('As variáveis numeroDez e stringDez não tem o mesmo valor')
}

````


## Utilizei o comparador ===
Diferentemente do comparador de igualdade == no qual a condição só será verdadeira se o valor da esquerda for o mesmo valor da direita, o "idêntico a" (===) vai fazer essa validação tendo certeza de que o número da direita é realmente um número, e não apenas possui o mesmo caractere.

- **“idêntico a”** (===). Ele não só compara os valores dos dois lados da equação, como também verifica se eles são do mesmo tipo. Por exemplo:

````javascript
let numeroUm = 1
let stringUm = '1'
let numeroTrinta = 30
let stringTrinta = '30'
let numeroDez = 10
let stringDez = '10'

if (numeroUm === stringUm) {
  console.log('As variáveis numeroUm e stringUm tem o mesmo valor, mas tipos diferentes')
} else {
  console.log('As variáveis numeroUm e stringUm não tem o mesmo valor')
}

if (numeroTrinta === stringTrinta) {
  console.log('As variáveis numeroTrinta e stringTrinta tem o mesmo valor e mesmo tipo')
} else {
  console.log('As variáveis numeroTrinta e stringTrinta não tem o mesmo tipo')
}

if (numeroDez === stringDez) {
  console.log('As variáveis numeroDez e stringDez tem o mesmo valor, mas tipos diferentes')
} else {
  console.log('As variáveis numeroDez e stringDez não tem o mesmo valor')
}
````



#7DaysOfCode - Lógica JS 2/7: 👩🏽‍💻 Variáveis

O site deve pedir para o usuário responder 3 perguntas:

- Qual o seu nome?
- Quantos anos você tem?
- Qual linguagem de programação você está estudando?

À medida que as perguntas forem sendo feitas, a pessoa que estiver usando o programa deve responder cada uma delas.

No final, o sistema vai exibir a mensagem:

**"Olá [nome], você tem [idade] anos e já está aprendendo [linguagem]!"**

Note que cada informação entre [ ] é uma das respostas dadas pela pessoa.

````javascript
let nome = prompt('Qual o seu nome? ')
let idade = prompt('Quantos anos você tem? ')
let linguagem = prompt('Qual linguagem de programação você está estudando? ')

console.log(`Olá ${nome}, você tem ${idade} anos e já está aprendendo ${linguagem}!`)
````

## Desafio extra

Se você quiser se aprofundar no assunto de hoje, eu tenho mais um exercício para você.

Você vai complementar o código para que, depois de exibir a mensagem anterior, o programa pergunte:

**Você gosta de estudar [linguagem]? Responda com o número 1 para SIM ou 2 para NÃO.**

E aí, dependendo da resposta, ele deve mostrar uma das seguintes mensagens:

**1 > Muito bom! Continue estudando e você terá muito sucesso.**
**2 > Ahh que pena... Já tentou aprender outras linguagens?**

````javascript
let pergunta = prompt(`Você gosta de estudar ${linguagem}? Responda com o número 1 para SIM ou 2 para NÃO.
`)

if (pergunta == 1){
    console.log("Muito bom! Continue estudando e você terá muito sucesso.")
} else if(pergunta == 2){
    console.log("Ahh que pena... Já tentou aprender outras linguagens?")
}

````
