### **Atividade de Back-End: Sistema de Cadastro de Planetas para Habitação Humana em Caso de Apocalipse**

### **Contexto:**

O planeta Terra está à beira de um colapso devido às queimadas e ao aquecimento global. Em uma tentativa desesperada de garantir a sobrevivência da humanidade, cientistas ao redor do mundo começaram a pesquisar planetas em outras galáxias que possam sustentar a vida humana. Sua missão é desenvolver um sistema de cadastro desses planetas candidatos à habitação. O sistema permitirá que novos planetas sejam cadastrados, listados, atualizados e excluídos. Cada planeta deverá ser avaliado com base em fatores como temperatura média, presença de água, e composição atmosférica.

### **Requisitos do Sistema:**

O sistema deve atender aos seguintes requisitos:

1. **Cadastrar Planetas:**
    - Os planetas devem ser cadastrados com as seguintes informações: nome, temperatura média, presença de água (true/false) e composição atmosférica.
    - Validação: Nome do planeta e temperatura são campos obrigatórios e a presença de água deve ser indicada como "sim" ou "não".
2. **Listar Planetas:**
    - Deve ser possível listar todos os planetas já cadastrados no sistema.
3. **Buscar Planeta Específico:**
    - Deve ser possível buscar um planeta específico pelo seu ID.
4. **Atualizar Planeta:**
    - O sistema deve permitir atualizar as informações de um planeta específico, exceto o ID.
    - Validação: Mesmas regras de cadastro (nome e temperatura obrigatórios e presença de água como "sim" ou "não").
5. **Excluir Planeta:**
    - Deve ser possível excluir um planeta específico do sistema, buscando-o pelo ID.

### **Instruções:**

1. **Defina as Rotas:**
    - Crie uma rota específica para cada funcionalidade e defina qual o método HTTP adequado para cada ação. As rotas podem seguir o padrão: `POST /planetas`, `GET /planetas`, `GET /planetas/:id`, `PUT /planetas/:id`, `DELETE /planetas/:id`.
    2. **Escolha os Métodos de Requisição:**
    - **POST**: Para cadastrar um novo planeta.
    - **GET**: Para listar todos os planetas e buscar um planeta específico.
    - **PUT**: Para atualizar as informações de um planeta.
    - **DELETE**: Para remover um planeta do sistema.
3. **Validação:**
    - Verifique se todos os campos obrigatórios (nome, temperatura, presença de água) estão preenchidos.
    - A presença de água deve ser "sim" ou "não".
4. **Códigos de Status HTTP:**
- **200 OK**: Operações de listagem, busca, atualização e exclusão bem-sucedidas.
- **201 Created**: Para indicar que o planeta foi cadastrado com sucesso.
- **400 Bad Request**: Quando há um erro de validação (ex: temperatura não especificada, campos obrigatórios não preenchidos).
- **404 Not Found**: Se o planeta não for encontrado na busca ou na tentativa de atualização/exclusão.
- **500 Internal Server Error**: Para capturar quaisquer outros erros inesperados no servidor.

---

### **Dicas:**

- Use o método `POST` para criar novos candidatos e o método `GET` para listar e buscar candidatos.
- Use `PUT` para atualizar e `DELETE` para excluir candidatos.
- Aplique a validação de idade e dos campos obrigatórios dentro das funções de criação e atualização.
- Retorne os códigos de status adequados, como `201 Created` para um novo candidato ou `404 Not Found` se um ID não for encontrado.