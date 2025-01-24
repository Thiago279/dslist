
# GameList - Projeto de Listagem de Jogos

Este projeto foi desenvolvido durante a **Imersão Java Spring** ministrada por **Nélio Alves**. Ele consiste em uma aplicação backend para gerenciar uma lista de jogos, incluindo funcionalidades como listagem por categorias e reordenamento de posições.

---

## 🚀 Tecnologias utilizadas

O projeto foi desenvolvido utilizando:

- **Java Spring**: Framework para desenvolvimento backend.
- **Spring Web**: Para manipulação de APIs REST.
- **Spring Data JPA**: Para integração com bancos de dados.
- **H2 Database**: Banco de dados em memória, ideal para testes locais.
- **PostgreSQL**: Banco de dados utilizado para implantação na nuvem.
- **Docker**: Contêinerização da aplicação, incluindo integração com PostgreSQL e PGAdmin.

---

## 📖 Funcionalidades principais

1. **Listagem de Jogos**:
   - O banco de dados armazena informações como nome, descrição, ano de lançamento, rating, entre outros.
   - Os jogos estão organizados em listas separadas por categorias (ex.: ação, plataforma).

2. **Reordenamento de Jogos**:
   - Possibilidade de alterar a posição de um jogo dentro de uma lista.
   - As alterações são refletidas e atualizadas diretamente no banco de dados.

3. **APIs RESTful**:
   - O projeto segue os padrões REST para organização e desenvolvimento da camada de controller.
   - As requisições HTTP podem ser testadas através de ferramentas como **Postman**.

---

## 🛠 Estrutura do Projeto

A aplicação foi desenvolvida em camadas para seguir boas práticas de arquitetura:

- **Controller**: Gerencia as requisições HTTP e segue os padrões REST.
- **Service**: Contém a lógica de negócios da aplicação.
- **Repository**: Responsável pela comunicação com o banco de dados.

---

## 🧪 Testes e Validação

- Durante o desenvolvimento, a aplicação foi testada utilizando o **H2 Database** para simulação de dados em memória.
- Para a implantação em ambientes de produção, o projeto utiliza o **PostgreSQL** como banco de dados principal.

---

## 🐳 Docker

O projeto utiliza o Docker para criar dois containers que comunicam entre si:

1. **PostgreSQL**: Servidor de banco de dados.
2. **PGAdmin**: Interface gráfica para gerenciar o banco de dados via navegador.

### Como usar o Docker:

1. Certifique-se de ter o Docker instalado em sua máquina.
2. No diretório do projeto, execute:
   ```bash
   docker-compose up
   ```
3. Isso irá iniciar:
   - O servidor PostgreSQL.
   - A interface gráfica PGAdmin, acessível no navegador em `http://localhost:5050`.

4. **Configuração do PGAdmin**:
   - Após acessar o PGAdmin no navegador, configure o servidor do PostgreSQL utilizando as credenciais definidas no arquivo `docker-compose.yml`.

---

## 🌐 Como usar a aplicação

1. **Clonar o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/gamelist
   cd gamelist
   ```

2. **Configurar o ambiente**:
   - Escolha o banco de dados a ser utilizado: H2 para testes locais ou PostgreSQL para ambientes Docker/nuvem.
   - Atualize as propriedades no arquivo `application.properties` conforme necessário.

3. **Rodar a aplicação**:
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Testar as requisições**:
   - Utilize ferramentas como **Postman** para testar os endpoints REST.
   - Endpoints disponíveis:
     - `GET /games`: Listar todos os jogos.
     - `POST /games`: Adicionar um novo jogo.
     - `PUT /games/{id}/move`: Alterar posição de um jogo em uma lista.

---

## 🌐 Implantação na nuvem

O projeto pode ser facilmente implantado em plataformas de nuvem que suportam:

- **PostgreSQL**: Para o banco de dados.
- **Docker**: Para contêineres.



