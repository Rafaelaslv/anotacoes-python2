 ## 📣 Hey!!

---

### Este repositório conterá minhas anotações dos conhecimentos obtidos sobre Python através da plataforma Descomplica.

---

#### CONDICIONAIS

Uma condição é algo que precisa ser atendido para que uma outra ação aconteça.

Então para que uma ação seja excecutada, uma outra ação precisa ser verdadeira.

SE CHOVER, SAIO COM GUARDA-CHUVA
SE NÃO CHOVER, NÃO SAIO COM GUARDA-CHUVA

As condicionais apontam condições que impõem uma regra a ser analisada para então escolher um caminho a seguir. Por padrão, as condicionais terão sempre duas saídas: ou elas serão verdadeiras ou elas serão falsas.

Entenda as condicionais como uma estrada na qual, ao chegar em seu fim, existem duas vias, sendo uma à direita e outra à esquerda. Neste cenário, observa-se alguns fatos:

Deve-se escolher uma das opções
Não é possível escolher ambas opções ao mesmo tempo
Caso a via da esquerda seja escolhida, a da direita será descartada
Caso a via da direita seja escolhida, a da esquerda será descartada
Ao se escolher uma via, toda a estrutura da via concorrente nunca será visitada

Agora traga esse cenário fictício para dentro do mundo computacional, aplicando a mesma lógica a um exemplo bastante trivial que experimentamos praticamente todos os dias: fazer o login em alguma área restrita (e-mail, rede social, plataformas diversas, etc.).

Pressuponha a existência de dois campos: usuário e senha Quais os critérios necessários para que o login seja realizado com sucesso?

Se você respondeu algo como “o usuário digitado deve corresponder ao usuário armazenado em banco de dados e a senha digitada deve corresponder à senha armazenada em banco de dados”, então sua resposta está correta!

Observe que no meio desta frase existem algumas palavras-chave e essas palavras-chave você precisa, ou notá-las, entender que serão utilizadas de alguma forma. Neste caso, as palavras-chave mencionadas são: “se”, “e” e “igual”.

O “se” é a nossa condição, uma vez que para algo acontecer, a condição deverá ser satisfeita: “O login deverá ser realizado apenas SE…”. Porém, existem duas regras para que o login seja realizado: tanto o usuário quanto a senha devem corresponder, respectivamente, aos valores previamente armazenados em banco de dados.

Dessa forma, não basta apenas o usuário estar correto, a senha também precisa estar. Da mesma maneira, não basta apenas a senha estar correta, o usuário também precisa estar. Obviamente, o pior cenário seria aquele em que nem o usuário e nem a senha estivessem corretos; definitivamente a área restrita não seria carregada neste caso!

Esta análise de regras tem uma ligação direta com a Lógica Proposicional - este tema eu abordo em meu canal no Youtube e você pode dar uma conferida lá acessando o link disponível no Módulo 8 deste material.

OS TIPOS DE CONDICIONAIS:

IF/Else
Switch Case(match)
Ternário

PODEMOS TER AFIRMAÇÕES COMPOSTAS:
SE CHOVER E (ESSE E É OS 2 E'S COMERCIAIS, DO OPERADOR DO TIPO LÓGICO) FOR DOMINGO SAIO COM GUARDA-CHUVA
SE NÃO CHOVER, NÃO SAIO COM GUARDA-CHUVA

E PODEMOS TER ESSAS PROPOSIÇÕES DE FORMA SIMPLES:
SE CHOVER, SAIO COM GUARDA-CHUVA
SE NÃO CHOVER, NÃO SAIO COM GUARDA-CHUVA

---

### IF/ELSE

Veja a sintaxe a seguir:

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

### TIPOS DE CONDICIONAIS

Para fins de otimização do algoritmo, pode-se melhorar essa mesma estrutura utilizando um recurso que na programação chamamos de “ou se” e, no Python, é conhecido como “elif” (uma versão curta de um “else if”, bastante comum em outras linguagens.

O elif propõe opções extras para a condicional, permitindo que o algoritmo decida por caminhos paralelos caso a primeira verificação resulte em falsa.

O comando elif tem praticamente o mesmo escopo que o IF, porém, analisa outras regras.

É importante que você compreenda que, assim que uma condicional atender aos requisitos, ou seja, obtiver saída verdadeira, ela para sua execução, ou seja, se, porventura, o elif da linha 32 vier a ser executado (caso o usuário tenha digitado o usuário correto mas a senha incorreta), todo o restante do bloco de condições não será invocado. Lembra-se do exemplo das vias? Se uma das vias for tomada, a outra será descartada.

Assim que uma condicional atender aos requisitos, ou seja, obtiver saída verdadeira, ela para sua execução, ou seja, se, porventura, o elif da linha 32 vier a ser executado (caso o usuário tenha digitado o usuário correto mas a senha incorreta), todo o restante do bloco de condições não será invocado.

Existe ainda o que chamamos de condicionais encadeadas, que basicamente são condicionais dentro de condicionais. Essa estrutura acaba sendo um pouco mais complexa mas é perfeitamente funcional.

Diferentemente da forma anterior, temos agora uma estrutura principal com apenas um IF e um ELSE. Caso a condição da linha 48 seja atendida, o algoritmo encerra na linha 49, informando que o Login foi realizado com sucesso, porém, caso algum dos dados (ou ambos) estejam incorretos, o algoritmo é direcionado ao ELSE, da linha 50.

---

### CONDICIONAL DO TIPO TERNÁRIO

Uma condicional do tipo ternário é uma forma simplificada de se fazer uma verificação do tipo IF/ELSE.

Este recurso é utilizado quando se tem uma condição curta de, basicamente, duas possibilidades.

No caso do exemplo de usuário e senha, o ternário não seria o mais adequado, uma vez que neste exemplo existem 4 possíveis saídas.

Com essa condicional, é possível resolver em apenas uma linha o que você gasta 4 ou 5 linhas utilizando o if/else.

A estrutura segue a mesma lógica.

A estrutura de um ternário consiste em fazer uma pergunta e apontar o que ocorreria se a resposta fosse verdadeira ou falsa.

idade = 18
print("É MAIOR") if idade >= 18 else print("É MENOR")

Primeiro se descreve a ação a ser executada e depois se aponta a condição.

“Escreva ‘é um’ SE variável a for igual a 1, senão, escreva ‘não é 1’”.

Você pode usar o ternário quando você tiver uma situação de condicional em que você tem apenas 2 saídas, porque você condensa/compacta a estrutura do seu código.

O Python tem uma pegada de deixar a sintaxe muito mais limpa/diminuta, então se você conseguir deixar a sintaxe do Python que já é limpa e compacta e você conseguir deixar mais limpa e compacta ainda, melhor para você a nível de compreensão, processamento e armazenagem.

---

### SWITCH CASE (MATCH)

Um outro tipo de condicional amplamente utilizado é o que, em outras linguagens, chamamos de switch/case. No Python, este comando é conhecido como MATCH, que tenta localizar um determinado padrão e “permite que os programas extraiam informações de tipos de dados complexos, ramificando a estrutura de dados e apliquem ações específicas com base em diferentes formas de dados”.

A estrutura do Match é mais compacta que o IF/ELSE, o que torna seu uso bastante agradável por gerar um código mais compacto.

### O CONCEITO DE BLOCOS

Alguns casos, determinados comandos não ficam propriamente alinhados à esquerda da tela.

Este recurso é denominado indentação e serve basicamente para demonstrar de forma visual os blocos pais, filhos, netos, bisnetos, etc. Cada nível de recuo, representa um bloco hierárquico, ou seja, o bloco recuado PERTENCE ao bloco antecessor.

Na maioria das linguagens este recurso tem um apelo visual para orientar o programador, porém, em Python, esse recurso tem um apelo funcional, ou seja, se você não aplicar a indentação da forma correta, o seu código literalmente deixará de funcionar.

### TÓPICOS AVANÇADOS

A lógica de programação é a base para que você se torne um programador de excelência. Mas a lógica inicia fora na computação, você sabia disso? Todos os conceitos utilizados dentro da programação são, na verdade, originados aqui, no mundo real e alguns foram sabiamente levados para dentro da matemática, como a Lógica Proposicional.

A Lógica proposicional é a base necessária para que você domine com eficiência a Lógica de Programação, desta forma, deixarei aqui alguns vídeos que podem te ajudar nessa jornada. Esses vídeos são do meu canal, o CódigoCEO, no Youtube. https://www.youtube.com/watch?v=d8CkDq65zco&list=PLGz-ioJ5m_Xtt_9coiTu9mbXjFLrUvjpb

---

CÓDIGOS UTILIZADOS NA DISCIPLINA:  https://github.com/FaculdadeDescomplica/Python

---

### Referência Bibliográfica

Python.org. Mais controles e ferramentas. Disponível em <https://docs.python.org/3/tutorial/controlflow.html> . Acesso em 10/11/2022

Python.org. What 's New In Python 3.10. Disponível em <https://docs.python.org/3/whatsnew/3.10.html> (adaptado). Acesso em 10/11/2022
