 ## 📣 Hey!!

---

### Este repositório conterá minhas anotações dos conhecimentos obtidos sobre Python através da plataforma Descomplica.

---

#### CONDICIONAIS

O que são condicionais

---

usuario = "python"
senha = "123"

usuarioDigitado = input("Digite seu usuário: ")
senhaDigitada = input("Digite sua senha: ")

if usuarioDigitado == usuario and senhaDigitada == senha:
    print("Login realizado com sucesso")
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

---
