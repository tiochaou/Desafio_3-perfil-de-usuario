# 🧩 Desafio 3 – Perfil de Utilizador 🔐

Professor: Ignacio Antonio da Cunha Neto

aluno: Giovanni Allevi

📝 Sobre o Projeto

Este projeto consiste numa aplicação web em PHP desenvolvida para autenticação de utilizadores e personalização de perfil. A aplicação processa o formulário na própria página de login, armazena as preferências na sessão e protege o acesso a páginas restritas.

🚀 Funcionalidades

🔑 Autenticação de Utilizador: Validação das credenciais (usuario e senha) diretamente na base de dados exercicio.

🎨 Escolha da Cor de Fundo: Definição da cor de preferência (lightblue, lightgreen, lightcoral, lightyellow) diretamente no formulário de entrada.

🛡️ Controlo de Acesso: Proteção da página de perfil através da verificação de $_SESSION['usuario'].

👤 Perfil Personalizado: Exibição da mensagem de boas-vindas e aplicação dinâmica da cor de fundo selecionada na sessão.

🚪 Logout: Encerramento da sessão com session_destroy() e redirecionamento para o login.

🛠️ Tecnologias Utilizadas

PHP — Gestão de sessões, integração com MySQL e lógica de negócio.

MySQL / MariaDB — Armazenamento dos dados de acesso.

HTML5 / CSS — Estruturação de formulários e estilização inline.

📁 Estrutura de Ficheiros

Plaintext
├── 15d_login.php   # Formulario de login, seleção de cor e validação no BD

├── 15d_perfil.php  # Página restrita do utilizador com cor de fundo dinâmica

└── 15d_logout.php  # Encerramento seguro da sessão

🗄️ Configuração da Base de Dados

O projeto utiliza as seguintes definições de ligação ao MySQL:

Host: localhost

Utilizador: root

Palavra-passe: Senai@118

Base de Dados: exercicio

Estrutura SQL

SQL
CREATE DATABASE IF NOT EXISTS exercicio;
USE exercicio;

CREATE TABLE IF NOT EXISTS usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    usuario VARCHAR(50) NOT NULL,
    senha VARCHAR(255) NOT NULL
);

-- Utilizador de teste

INSERT INTO usuarios (usuario, senha) VALUES ('admin', '1234');
⚙️ Como Executar o Projeto
Configurar a Base de Dados:

Garanta que o servidor MySQL está em execução.

Crie a base de dados exercicio e a tabela usuarios utilizando o código SQL acima.

Iniciar o Servidor Web:

Coloque os ficheiros no diretório do seu servidor local (ex: htdocs no XAMPP) ou inicie o servidor embutido do PHP na pasta dos ficheiros:

Bash

php -S localhost:8000
