# Leitores — API

API REST da pesquisa de perfil de leitura [Leitores](https://github.com/JulianaElen/unifei-frontend-leitores).
Armazena os participantes e as respostas do questionário e fornece os dados para os
gráficos de resultados.

🔗 **Front-end:** [frontend-leitores.vercel.app](https://frontend-leitores.vercel.app)

## 🛠️ Tecnologias

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)

Node.js · Express · PostgreSQL (`pg`) · CORS · dotenv · deploy serverless na Vercel

## 📡 Endpoints

| Método | Rota | Descrição |
|---|---|---|
| `POST` | `/cadastro` | Cadastra um participante pelo e-mail |
| `GET` | `/cadastro/:email` | Busca um participante pelo e-mail |
| `DELETE` | `/cadastro/:id` | Remove um participante |
| `POST` | `/respostas` | Registra a resposta de um participante a uma pergunta |
| `GET` | `/respostas` | Lista todas as respostas |
| `GET` | `/respostas/usuario/:email` | Respostas de um participante |
| `GET` | `/respostas/pergunta/:pergunta_id` | Respostas de uma pergunta (usado nos gráficos) |

As consultas usam **parâmetros** (`$1`, `$2`…), protegendo contra SQL injection, e as
credenciais ficam em variáveis de ambiente.

## ▶️ Como executar

```bash
npm install
```

Crie um arquivo `.env`:

```env
PORT=3000
pgConnection=postgres://usuario:senha@host:5432/banco
```

```bash
node index.js
```
