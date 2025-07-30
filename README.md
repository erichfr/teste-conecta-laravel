# Teste Conecta - API RESTful com Laravel 10

Este projeto é uma API RESTful desenvolvida em **Laravel 10** como parte do processo seletivo para empresa Conecta Lá. A API permite **criar, listar, atualizar e deletar usuários**, utilizando **MySQL** como banco de dados.

---

## Tecnologias

- PHP 8.1+
- Laravel 10
- MySQL
- Composer

---

## Instalação

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/teste-conecta.git
cd teste-conecta
```
2. Instale as dependências:
```bash
composer install
```
3. Copie o arquivo .env e configure:
```bash
cp .env.example .env

DB_DATABASE=teste_conecta
DB_USERNAME=
DB_PASSWORD=
```
4. Gere a key da aplicação:
```bash
php artisan key:generate
```
5. Rode as migrations:
```bash
php artisan migrate
```
6. Suba o servidor local:
```bash
php artisan serve
```

## Endpoints da API

| Método | Endpoint          | Ação                      |
| ------ | ----------------- | ------------------------- |
| GET    | `/api/users`      | Listar todos os usuários  |
| GET    | `/api/users/{id}` | Ver um usuário específico |
| POST   | `/api/users`      | Criar um novo usuário     |
| PUT    | `/api/users/{id}` | Atualizar um usuário      |
| DELETE | `/api/users/{id}` | Deletar um usuário        |

## Exemplo de JSON para criar/atualizar

```bash
{
  "name": "Augusto Malta",
  "email": "malta@email.com",
  "password": "123456"
}
```

## Validações

- Name: obrigatório, texto.
- E-mail: obrigatório, formato válido, único.
- Password: obrigatório no cadastro, mínimo 6 caracteres.

## Segurança

- Senhas são armazenadas com hash (bcrypt).
- Validação e tratamento de erros inclusos.
