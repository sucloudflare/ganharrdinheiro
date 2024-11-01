# Projeto de Cadastro de Usuários - Curso Lucrativo

Este é um projeto de cadastro de usuários para uma página de divulgação de um curso, onde os usuários podem se inscrever gratuitamente e visualizar informações sobre o curso. Além disso, o sistema possui uma área de login que permite, mediante senha correta, visualizar todos os usuários cadastrados.

## Funcionalidades

- **Cadastro de Usuário**: Permite que novos usuários se registrem com dados como nome, email, número de telefone e senha.
- **Armazenamento Local**: As informações dos usuários são armazenadas localmente no navegador usando `localStorage`.
- **Verificação de Senha**: Após o cadastro, a lista de usuários só é exibida mediante a inserção de uma senha correta.
- **Comentários dos Alunos**: Exibe comentários fictícios de alunos sobre a experiência com o curso.

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos:

- `index.html`: Contém a estrutura HTML da página.
- `styles.css`: Estilização do layout e dos elementos da página.
- `script.js`: Código JavaScript que gerencia o funcionamento do cadastro de usuários, verificação de senha e exibição de usuários.

## Tecnologias Utilizadas

- **HTML**: Para a estrutura da página.
- **CSS**: Para estilizar e organizar a página visualmente.
- **JavaScript**: Para a lógica de manipulação dos dados, validação de senha e exibição de usuários.
- **LocalStorage**: Para armazenamento dos dados dos usuários no navegador.

## Como Usar

### Cadastro:

1. Abra o arquivo `index.html` em um navegador.
2. Preencha o formulário com nome, email, número e senha.
3. Clique em "Cadastrar" para salvar os dados do usuário.

### Verificar Usuários:

1. Vá até a seção "Digite a senha" no final da página.
2. Insira a senha correta no campo indicado e clique em "Usuário".
3. Se a senha estiver correta, a lista de usuários cadastrados será exibida.

### Senha de Acesso:

A senha padrão para visualizar os usuários é `Zx1952@@@@`.

## Exemplo de Código

### Estrutura HTML para Cadastro

```html
<form id="registration-form">
    <label for="name">Nome:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="phone">Número:</label>
    <input type="tel" id="phone" name="phone" required>
    
    <label for="password">Senha:</label>
    <input type="password" id="password" name="password" required>
    
    <label for="confirm-password">Confirmar Senha:</label>
    <input type="password" id="confirm-password" name="confirm-password" required>
    
    <button type="submit">Cadastrar</button>
</form>




´´´




JavaScript para Exibir Usuários


´´´´
function displayUsers() {
    const userList = document.getElementById('userList');
    const usuarios = JSON.parse(localStorage.getItem('usuarios')) || [];
    userList.innerHTML = ''; 

    usuarios.forEach(usuario => {
        const userDiv = document.createElement('div');
        userDiv.classList.add('user-item');
        userDiv.innerHTML = `
            <p><strong>Nome:</strong> ${usuario.name}</p>
            <p><strong>Email:</strong> ${usuario.email}</p>
            <p><strong>Número:</strong> ${usuario.phone}</p>
            <p><strong>Senha:</strong> ${usuario.password}</p>
            <hr>
        `;
        userList.appendChild(userDiv);
    });
}

´´´´




Melhorias Futuras
Autenticação mais segura: Implementar autenticação com criptografia para as senhas dos usuários.
Banco de Dados: Migrar o armazenamento dos dados para um banco de dados para maior segurança e escalabilidade.
Validação de Formulário: Adicionar validações mais avançadas para o formulário de cadastro.
Requisitos
Navegador com suporte a HTML5, CSS3 e JavaScript.
Conexão com internet para acessar dependências externas (opcional).
Autor
Edson Bruno


Este arquivo `README.md` fornece uma descrição completa do projeto, suas funcionalidades, estrutura e instruções de uso.
