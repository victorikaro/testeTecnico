# Teste Técnico — Python

**Tempo estimado:** 2 a 3 horas  
**Linguagem:** Python 3.10+  
**Entrega:** Repositório Git ou arquivo `.zip`  
**Bibliotecas externas:** Permitidas, desde que justificadas  

---

## Contexto

Você foi contratado para desenvolver um pequeno **sistema de gerenciamento de usuários** para uma aplicação interna.  
O sistema deve permitir cadastro, listagem, busca e análise simples de dados.

---

## Requisitos Gerais

- Código limpo e legível  
- Uso de funções e/ou classes  
- Tratamento básico de erros  
- Comentários apenas quando necessário  
- Não utilizar `input()` diretamente dentro da lógica principal  
- Separar interface (CLI) da lógica de negócio  

---

## Parte 1 — Modelagem de Dados

Crie uma classe chamada `User` com os seguintes atributos:

- `id` (int)  
- `name` (str)  
- `email` (str)  
- `age` (int)  
- `active` (bool)  

### Regras

- O email deve conter `@`  
- A idade deve ser maior que 0  
- O `id` deve ser único  

---

## Parte 2 — Gerenciamento de Usuários

Crie uma classe `UserManager` responsável por gerenciar os usuários.

### Métodos Obrigatórios

#### `add_user(user: User) -> None`
- Adiciona um usuário à lista  
- Não permitir emails duplicados  

#### `remove_user(user_id: int) -> bool`
- Remove um usuário pelo ID  
- Retorna `True` se removeu  
- Retorna `False` se não encontrou  

#### `get_active_users() -> list[User]`
- Retorna apenas usuários ativos  

#### `find_user_by_email(email: str) -> User | None`
- Busca um usuário pelo email  

---

## Parte 3 — Análise de Dados

Implemente funções que:

1. Retornem a **idade média** dos usuários ativos  
2. Retornem o **usuário mais velho**  
3. Agrupem usuários por faixa etária:
   - 0–17  
   - 18–30  
   - 31–50  
   - 51+  

---

## Parte 4 — Persistência (Obrigatório)

Implemente salvamento e leitura dos usuários em **JSON**.

### Métodos Esperados

- `save_to_file(path: str)`  
- `load_from_file(path: str)`  

---

## Parte 5 — Desafio Extra (Diferencial)

Escolha **apenas uma opção**:

### Opção A — CLI
Crie uma interface simples no terminal que permita:
- Criar usuário  
- Listar usuários  
- Remover usuário  
- Salvar e carregar dados  

### Opção B — Testes
Implemente **testes unitários** utilizando:
- `unittest` **ou**
- `pytest`  

---

## Critérios de Avaliação

- Clareza e legibilidade do código  
- Organização do projeto  
- Correta implementação da lógica  
- Tratamento de erros  
- Aderência aos requisitos  
- Diferenciais implementados  

---

## Bônus (Opcional)

- Type hints completos  
- Uso de `dataclasses`  
- Validações mais robustas  
- README explicando decisões técnicas  

---

## Observações Finais

Este teste simula um desafio técnico real aplicado por empresas.  
Sinta-se à vontade para estruturar o projeto da forma que considerar mais adequada, desde que os requisitos sejam atendidos.
