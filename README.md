Forum Hub
Forum Hub é um software de fórum desenvolvido em Java, utilizando o framework Spring Boot. Este projeto tem como objetivo fornecer uma plataforma de discussão eficiente e escalável para comunidades online.

Funcionalidades
Criação de Tópicos: Permite que os usuários iniciem novas discussões sobre diversos assuntos.
Respostas: Os participantes podem responder aos tópicos existentes, promovendo interações e debates.
Categorias: Organização dos tópicos em categorias para facilitar a navegação e a busca por assuntos específicos.
Perfis de Usuário: Cada usuário possui um perfil onde suas atividades e informações básicas são exibidas.
Tecnologias Utilizadas
Java: Linguagem principal do projeto.
Spring Boot: Framework que simplifica a criação de aplicações Java robustas e escaláveis.
Maven: Ferramenta de automação de compilação utilizada para gerenciamento de dependências e construção do projeto.
Estrutura do Banco de Dados
O esquema do banco de dados é composto pelas seguintes tabelas principais:

cursos:

id (BIGINT): Identificador único do curso.
nome (VARCHAR): Nome do curso.
categoria (VARCHAR): Categoria à qual o curso pertence.
perfis:

id (BIGINT): Identificador único do perfil.
nome (VARCHAR): Nome do perfil.
respostas:

id (BIGINT): Identificador único da resposta.
mensagem (VARCHAR): Conteúdo da resposta.
data_criacao (DATETIME): Data e hora de criação da resposta.
solucao (VARCHAR): Indica se a resposta é uma solução.
autor_id (BIGINT): Referência ao usuário autor da resposta.
topico_id (BIGINT): Referência ao tópico ao qual a resposta pertence.
topicos:

id (BIGINT): Identificador único do tópico.
titulo (VARCHAR): Título do tópico.
mensagem (VARCHAR): Conteúdo inicial do tópico.
status (BIT): Status do tópico (ativo/inativo).
autor_id (BIGINT): Referência ao usuário autor do tópico.
curso_id (BIGINT): Referência ao curso relacionado ao tópico.
usuarios:

id (BIGINT): Identificador único do usuário.
nome (VARCHAR): Nome do usuário.
email (VARCHAR): Endereço de email do usuário.
senha (VARCHAR): Senha de acesso do usuário.
usuarios_perfis:

perfis_id (BIGINT): Referência ao perfil do usuário.
usuarios_id (BIGINT): Referência ao usuário.
Para mais detalhes sobre o esquema do banco de dados, consulte o modelo de esquema do Forum Hub.

Como Executar o Projeto
Pré-requisitos:

Java Development Kit (JDK) 11 ou superior instalado.
Maven instalado para gerenciamento de dependências.
Clonar o Repositório:

bash
Copiar
Editar
git clone https://github.com/Jader-Moura-Lattarulo/Forum-hub.git
Construir o Projeto: Navegue até o diretório do projeto e execute:

bash
Copiar
Editar
mvn clean install
Executar a Aplicação: Após a construção bem-sucedida, execute:

bash
Copiar
Editar
mvn spring-boot:run
Acessar a Aplicação: A aplicação estará disponível em http://localhost:8080.

Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

Licença
Este projeto está licenciado sob os termos da licença MIT. Consulte o arquivo LICENSE para mais informações.
