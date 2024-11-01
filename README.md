 <h1>Projeto de Cadastro de Usuários - Curso Lucrativo</h1>
    <p>Este é um projeto de cadastro de usuários para uma página de divulgação de um curso, onde os usuários podem se inscrever gratuitamente e visualizar informações sobre o curso. Além disso, o sistema possui uma área de login que permite, mediante senha correta, visualizar todos os usuários cadastrados.</p>

    <h2>Funcionalidades</h2>
    <ul>
        <li><strong>Cadastro de Usuário</strong>: Permite que novos usuários se registrem com dados como nome, email, número de telefone e senha.</li>
        <li><strong>Armazenamento Local</strong>: As informações dos usuários são armazenadas localmente no navegador usando <code>localStorage</code>.</li>
        <li><strong>Verificação de Senha</strong>: Após o cadastro, a lista de usuários só é exibida mediante a inserção de uma senha correta.</li>
        <li><strong>Comentários dos Alunos</strong>: Exibe comentários fictícios de alunos sobre a experiência com o curso.</li>
    </ul>

    <h2>Estrutura do Projeto</h2>
    <p>O projeto é composto pelos seguintes arquivos:</p>
    <ul>
        <li><code>index.html</code>: Contém a estrutura HTML da página.</li>
        <li><code>styles.css</code>: Estilização do layout e dos elementos da página.</li>
        <li><code>script.js</code>: Código JavaScript que gerencia o funcionamento do cadastro de usuários, verificação de senha e exibição de usuários.</li>
    </ul>

    <h2>Tecnologias Utilizadas</h2>
    <ul>
        <li><strong>HTML</strong>: Para a estrutura da página.</li>
        <li><strong>CSS</strong>: Para estilizar e organizar a página visualmente.</li>
        <li><strong>JavaScript</strong>: Para a lógica de manipulação dos dados, validação de senha e exibição de usuários.</li>
        <li><strong>LocalStorage</strong>: Para armazenamento dos dados dos usuários no navegador.</li>
    </ul>

    <h2>Como Usar</h2>

    <h3>Cadastro:</h3>
    <ol>
        <li>Abra o arquivo <code>index.html</code> em um navegador.</li>
        <li>Preencha o formulário com nome, email, número e senha.</li>
        <li>Clique em "Cadastrar" para salvar os dados do usuário.</li>
    </ol>

    <h3>Verificar Usuários:</h3>
    <ol>
        <li>Vá até a seção "Digite a senha" no final da página.</li>
        <li>Insira a senha correta no campo indicado e clique em "Usuário".</li>
        <li>Se a senha estiver correta, a lista de usuários cadastrados será exibida.</li>
    </ol>

    <h3>Senha de Acesso:</h3>
    <p>A senha padrão para visualizar os usuários é <code>Zx1952@@@@</code>.</p>

    <h2>Exemplo de Código</h2>

    <h3>Estrutura HTML para Cadastro</h3>
    <pre>
        <code>
            &lt;form id="registration-form"&gt;
                &lt;label for="name"&gt;Nome:&lt;/label&gt;
                &lt;input type="text" id="name" name="name" required&gt;
                
                &lt;label for="email"&gt;Email:&lt;/label&gt;
                &lt;input type="email" id="email" name="email" required&gt;
                
                &lt;label for="phone"&gt;Número:&lt;/label&gt;
                &lt;input type="tel" id="phone" name="phone" required&gt;
                
                &lt;label for="password"&gt;Senha:&lt;/label&gt;
                &lt;input type="password" id="password" name="password" required&gt;
                
                &lt;label for="confirm-password"&gt;Confirmar Senha:&lt;/label&gt;
                &lt;input type="password" id="confirm-password" name="confirm-password" required&gt;
                
                &lt;button type="submit"&gt;Cadastrar&lt;/button&gt;
            &lt;/form&gt;
        </code>
    </pre>

    <h3>JavaScript para Exibir Usuários</h3>
    <pre>
        <code>
            function displayUsers() {
                const userList = document.getElementById('userList');
                const usuarios = JSON.parse(localStorage.getItem('usuarios')) || [];
                userList.innerHTML = ''; 

                usuarios.forEach(usuario =&gt; {
                    const userDiv = document.createElement('div');
                    userDiv.classList.add('user-item');
                    userDiv.innerHTML = `
                        &lt;p&gt;&lt;strong&gt;Nome:&lt;/strong&gt; ${usuario.name}&lt;/p&gt;
                        &lt;p&gt;&lt;strong&gt;Email:&lt;/strong&gt; ${usuario.email}&lt;/p&gt;
                        &lt;p&gt;&lt;strong&gt;Número:&lt;/strong&gt; ${usuario.phone}&lt;/p&gt;
                        &lt;p&gt;&lt;strong&gt;Senha:&lt;/strong&gt; ${usuario.password}&lt;/p&gt;
                        &lt;hr&gt;
                    `;
                    userList.appendChild(userDiv);
                });
            }
        </code>
    </pre>

    <h2>Melhorias Futuras</h2>
    <ul>
        <li><strong>Autenticação mais segura</strong>: Implementar autenticação com criptografia para as senhas dos usuários.</li>
        <li><strong>Banco de Dados</strong>: Migrar o armazenamento dos dados para um banco de dados para maior segurança e escalabilidade.</li>
        <li><strong>Validação de Formulário</strong>: Adicionar validações mais avançadas para o formulário de cadastro.</li>
    </ul>

    <h2>Requisitos</h2>
    <ul>
        <li>Navegador com suporte a HTML5, CSS3 e JavaScript.</li>
        <li>Conexão com internet para acessar dependências externas (opcional).</li>
    </ul>

    <h2>Autor</h2>
    <p>Edson Bruno</p>
</body>
</html>
