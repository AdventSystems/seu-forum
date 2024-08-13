# Seu Forum

### Figma
https://www.figma.com/design/vT2HaaAnNmr49npHTSJlyb/Seu-Forum---Organi7e?node-id=0-1&t=F6YjVjewRHHCCKV5-1

### Levantamento de Requisitos para Sistema de Fórum

#### Funcionalidades Principais

1. **Cadastro e Autenticação de Usuários**
   - **Cadastro de Usuário**: Permitir que novos usuários se cadastrem no sistema com informações como nome, email, senha, etc.
   - **Login de Usuário**: Permitir que os usuários se autentiquem no sistema utilizando email e senha.
   - **Recuperação de Senha**: Permitir que os usuários possam recuperar suas senhas caso as esqueçam.

2. **Gerenciamento de Posts**
   - **Criação de Posts**: Usuários autenticados podem criar novos posts.
   - **Visualização de Posts**: Todos os usuários (autenticados ou não) podem visualizar os posts.
   - **Edição de Posts**: Usuários podem editar seus próprios posts.
   - **Deleção de Posts**: Usuários podem deletar seus próprios posts.

3. **Gerenciamento de Comentários**
   - **Criação de Comentários**: Usuários autenticados podem comentar nos posts.
   - **Visualização de Comentários**: Todos os usuários podem visualizar os comentários.
   - **Edição de Comentários**: Usuários podem editar seus próprios comentários.
   - **Deleção de Comentários**: Usuários podem deletar seus próprios comentários.

4. **Pesquisa e Filtros**
   - **Pesquisa por Posts**: Implementar uma funcionalidade de pesquisa que permita aos usuários buscar por posts utilizando palavras-chave.
   - **Filtros**: Adicionar filtros para categorizar posts por data, popularidade, autor, etc.

5. **Perfis de Usuário**
   - **Visualização de Perfil Pessoal**: Usuários autenticados podem visualizar e editar seu próprio perfil.
   - **Visualização de Perfil de Outros Usuários**: Todos os usuários podem visualizar o perfil de outros usuários, mas apenas informações limitadas (ex.: nome, posts, etc.).

#### Requisitos Não Funcionais

1. **Segurança**
   - **Autenticação e Autorização**: Implementar autenticação segura e controle de acesso para garantir que apenas usuários autenticados possam criar ou comentar posts.
   - **Proteção de Dados**: Assegurar a proteção de dados pessoais dos usuários.
   - **Prevenção de Ataques**: Implementar medidas de segurança contra ataques comuns, como SQL Injection, Cross-Site Scripting (XSS), e Cross-Site Request Forgery (CSRF).

2. **Desempenho**
   - **Escalabilidade**: O sistema deve ser capaz de lidar com um grande número de usuários e posts.
   - **Tempo de Resposta**: O sistema deve proporcionar tempos de resposta rápidos para todas as operações.

3. **Usabilidade**
   - **Interface Intuitiva**: A interface do usuário deve ser intuitiva e fácil de usar.
   - **Acessibilidade**: O sistema deve ser acessível para usuários com diferentes necessidades.

4. **Manutenção**
   - **Documentação**: O código deve ser bem documentado para facilitar a manutenção futura.
   - **Modularidade**: O sistema deve ser modular para permitir a fácil adição de novas funcionalidades.

#### Tecnologias e Ferramentas Recomendadas

1. **Frontend**
   - Framework: Vue.js
   - Gerenciamento de Estado: Pinia
   - Estilização: SCSS, Tailwind CSS
   - Bibliotecas Adicionais: Vue Router para roteamento, VueUse para utilitários

2. **Backend**
   - Framework: Laravel
   - Banco de Dados: MySQL ou PostgreSQL
   - Autenticação: Laravel Sanctum ou Passport

3. **Infraestrutura**
   - Servidor: Nginx ou Apache
   - Hospedagem: AWS, DigitalOcean ou Heroku
   - CI/CD: GitHub Actions, GitLab CI/CD

#### Exemplo de Estrutura de Dados

1. **Usuário**
   - ID
   - Nome
   - Email
   - Senha (hash)
   - Data de Criação
   - Data de Atualização

2. **Post**
   - ID
   - Título
   - Conteúdo
   - ID do Autor (Usuário)
   - Data de Criação
   - Data de Atualização

3. **Comentário**
   - ID
   - Conteúdo
   - ID do Autor (Usuário)
   - ID do Post
   - Data de Criação
   - Data de Atualização

**OBS: Esta é uma base para o levantamento de requisitos do sistema de fórum.**
