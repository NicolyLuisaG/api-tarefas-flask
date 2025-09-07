# API de Tarefas - Spring Boot

Este projeto implementa uma API RESTful para gerenciamento de tarefas desenvolvida em Java com Spring Boot.

## Aluna
- **Nome:** Nicoly Santos
- **RU:** 4732999
- **Cidade:** Limeira - São Paulo

## Descrição

A API permite realizar operações CRUD (Create, Read, Update, Delete) em tarefas, contendo as seguintes informações:
- Nome da tarefa
- Data de entrega
- Responsável pela tarefa

## Tecnologias Utilizadas

- Java 11
- Spring Boot 2.7.0
- Spring Data JPA
- H2 Database (em memória)
- Maven

## Endpoints da API

### Criar uma nova tarefa
```
POST /api/tarefas
Content-Type: application/json

{
  "nome": "Nome da tarefa",
  "dataEntrega": "2025-12-12",
  "responsavel": "Nome do responsável"
}
```

### Listar todas as tarefas
```
GET /api/tarefas
```

### Buscar tarefa por ID
```
GET /api/tarefas/{id}
```

### Atualizar uma tarefa
```
PUT /api/tarefas/{id}
Content-Type: application/json

{
  "nome": "Nome atualizado",
  "dataEntrega": "2025-12-15",
  "responsavel": "Responsável atualizado"
}
```

### Excluir uma tarefa
```
DELETE /api/tarefas/{id}
```

## Como executar

1. Clone o repositório
2. Execute `mvn clean install` para instalar as dependências
3. Execute `mvn spring-boot:run` para iniciar a aplicação
4. A API estará disponível em `http://localhost:8080`

## Banco de Dados

O projeto utiliza H2 Database em memória para facilitar os testes. O console do H2 pode ser acessado em:
- URL: `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (vazio)

## Testes

Os testes foram realizados utilizando Hoppscotch (alternativa ao Postman) e demonstram todas as funcionalidades da API:

1. **Teste 1:** Criação de 3 tarefas, incluindo a tarefa "Desenvolvimento da API" com responsável "Nicoly 4732999"
2. **Teste 2:** Listagem de todas as tarefas cadastradas
3. **Teste 3:** Atualização da tarefa com nome da aluna
4. **Teste 4:** Exclusão da tarefa e verificação da remoção da lista

## Estrutura do Projeto

```
src/
├── main/
│   ├── java/
│   │   └── com/example/apitarefas/
│   │       ├── ApiTarefasApplication.java
│   │       ├── controller/
│   │       │   └── TarefaController.java
│   │       ├── model/
│   │       │   └── Tarefa.java
│   │       └── repository/
│   │           └── TarefaRepository.java
│   └── resources/
│       └── application.properties
└── test/
```


