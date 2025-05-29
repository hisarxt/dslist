# 🎮 DSList

Projeto desenvolvido com Spring Boot para listar e organizar jogos, com backend completo e integração com banco de dados.

> Projeto feito durante o curso **Java Spring Boot** da [DevSuperior](https://devsuperior.com.br/).

## 📌 Sobre o Projeto

O **DSList** é uma API REST que permite:

- Listar jogos com informações como título, score, gênero, descrição, imagem, etc.
- Criar e gerenciar listas personalizadas de jogos.
- Reordenar os jogos nas listas por posição.

## 🛠️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **PostgreSQL**
- **H2 Database (para testes)**
- **Lombok**
- **ModelMapper**


## 📄 Funcionalidades

- [x] Listar todos os jogos
- [x] Listar jogos por ID
- [x] Listar jogos por lista
- [x] Criar novas listas
- [x] Atualizar posição de jogos nas listas

## 🔧 Como Executar

### Pré-requisitos

- Java 17 instalado
- Maven instalado
- PostgreSQL rodando (ou usar H2 para testes rápidos)

### Passos

```bash
# Clone o repositório
git clone https://github.com/hisarxt/dslist.git
cd dslist

# Execute o projeto
./mvnw spring-boot:run
```

---

## ⚙️ Configuração do Banco de Dados

O projeto usa o banco H2 em memória por padrão.  
Para usar PostgreSQL, edite o arquivo `src/main/resources/application.properties` com suas credenciais:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dslist
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

## 🧪 Exemplos de Endpoints

```http
GET /games
# Lista todos os jogos

GET /games/{id}
# Detalhes de um jogo específico

GET /lists
# Lista todas as listas de jogos

GET /lists/{listId}/games
# Jogos dentro de uma lista específica

POST /lists/{listId}/replacement
# Atualiza a ordem dos jogos na lista
```

---

## 📸 Imagens

Abaixo alguns exemplos do funcionamento da API via Postman:

### 🔍 Listagem de Jogos
![Listagem de jogos](./assets/listagem-jogos.png)

### 🎯 Detalhes de um Jogo
![Detalhes do jogo](./assets/detalhes-jogo.png)

### 📋 Listas de Jogos
![Listas de jogos](./assets/listas-jogos.png)

> 📝 Coloque suas imagens na pasta `assets/` no diretório raiz do projeto, ou ajuste os caminhos conforme necessário.

---

## 🙋 Autor

Desenvolvido por [Arthur Fernandes](https://github.com/hisarxt)  
- 📧 Email: artufa74@gmail.com 
- 📎 LinkedIn: [linkedin.com/in/artxrz/](https://www.linkedin.com/in/artxrz/)

Se você gostou do projeto, sinta-se à vontade para deixar uma ⭐ no repositório!





