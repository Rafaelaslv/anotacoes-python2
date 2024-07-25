 ## 📣 Hey!!

---

### Este repositório conterá minhas anotações dos conhecimentos obtidos sobre Python através da plataforma Descomplica.

---

#### CONDICIONAIS

As condicionais apontam condições que impõem uma regra a ser analisada para então escolher um caminho a seguir. Por padrão, as condicionais terão sempre duas saídas: ou elas serão verdadeiras ou elas serão falsas.

Entenda as condicionais como uma estrada na qual, ao chegar em seu fim, existem duas vias, sendo uma à direita e outra à esquerda. Neste cenário, observa-se alguns fatos:

Deve-se escolher uma das opções
Não é possível escolher ambas opções ao mesmo tempo
Caso a via da esquerda seja escolhida, a da direita será descartada
Caso a via da direita seja escolhida, a da esquerda será descartada
Ao se escolher uma via, toda a estrutura da via concorrente nunca será visitada

---

usuario = "python"
senha = "123"

usuarioDigitado = input("Digite seu usuário: ")
senhaDigitada = input("Digite sua senha: ")

if usuarioDigitado == usuario and senhaDigitada == senha:
    print("Login realizado com sucesso") - ESSE ESPAÇO QUE FICOU NA FRENTE DO PRINT É UMA INDENTAÇÃO (É UMA FORMA VISUAL DE MOSTRAR QUE UM DETERMINADO BLOCO PERTENCE A UM OUTRO BLOCO/COMO ESTÁ A UM NÍVEL PARA DENTRO, ESTOU DIZENDO QUE ESSE PRINT PERTENCE AO BLOCO DE CIMA). COM OUTRAS LINGUAGENS DE PROGRAMAÇÃO, SERVE MAIS PARA TER UMA ORGANIZAÇÃO VISUAL PARA ENTENDER QUEM PERTENCE A QUEM. JÁ NO PYTHON NÃO, POIS SE VOCÊ NÃO COLOCA A INDENTAÇÃO ELE NÃO FUNCIONA/DÁ ERRO. ENTÃO, SEMPRE QUE APARECER A PLAVRA INDENTAÇÃO EM ALGUM ERRO NO SEU CONSOLE, VOCÊ ESUECEU DE COLOCAR ESSE ESPAÇO OU COLOCOU ESPAÇO A MAIS. 
else:
    print("Erro ao realizar o login")

Observe que foram utilizados alguns conceitos em conjunto neste mesmo código:

A condicional em si, por meio do comando IF (que em uma tradução literal, para o Português, significa “se”);
O operador relacional de igualdade (==), que verifica se um dado A é igual a um outro dado B (no caso, comparando os usuários e comparando as senhas);
O operador “e”, que impõe a regra sobre ambas a saídas serem verdadeiras: tanto o usuário quanto a senha devem ser equivalentes aos seus correspondentes para que a saída global seja verdadeira.

Um elemento extra, chamado “else” é colocado na linha 32 da Figura 14. Esse else simboliza um “senão”, ou seja, um contraponto caso a condição seja falsa. Desta forma, o else seria executado para suprir a necessidade de algo acontecer caso o usuário não conseguisse logar. O else seria invocado se:

O usuário estivesse incorreto, mesmo com a senha correta;
A senha estivesse incorreta mesmo com o usuário correto;
O usuário e a senha estivessem incorretos

Veja, então, que a única possibilidade de este código ingressar dentro do bloco do IF, é se ambas as verificações forem verdadeiras.

TEMOS TAMBÉM O ELIF QUE É UMA JUNÇÃO DO ELSE COM O IF.
VOCÊ PODE TER QUANTOS ELIF'S VOCÊ QUISER DESDE QUE ESTEJA ENTRE O IF E O ELSE., MAS QUANTO MAIOR SEU BLOCO DE CONDIÇÕES, MAIS TEMPO O ALGORITMO FICARÁ PROCESSANDO.
É PARA QUANDO TEM MAIS DE 2 CONDIÇÕES.

---
