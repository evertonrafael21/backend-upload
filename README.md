# Backend Upload de Arquivos (Node.js + MySQL)

Este é um backend simples para upload de arquivos, feito com Node.js, Express, MySQL e Multer. Ideal para integrar com um front-end (ex: feito no Base44).

## 🚀 Tecnologias

- Node.js
- Express
- Multer (upload de arquivos)
- MySQL (armazenamento dos metadados)
- CORS
- ESModules

---

## 📦 Instalação

1. Clone este repositório ou baixe o .zip
2. Vá até a pasta `backend/`
3. Instale as dependências:
   ```bash
   npm install
   ```

---

## ⚙️ Configuração do Banco de Dados

Edite as credenciais do banco no `index.js`:
```js
const db = await mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "sua_senha",
  database: "fleetflow"
});
```

A tabela `files` será criada automaticamente ao iniciar o servidor.

---

## ▶️ Rodar o servidor

```bash
npm start
```

Servidor estará disponível em:  
📍 `http://localhost:3001`

---

## 📡 Rotas da API

### `POST /api/upload`
- Upload de um arquivo
- Enviar como `multipart/form-data` com campo `file`

### `GET /api/files`
- Lista os arquivos cadastrados
- Query params opcionais:
  - `page` (padrão: 1)
  - `limit` (padrão: 10)

### `GET /api/preview/:filename`
- Retorna o conteúdo do arquivo (útil para preview)

---

## 🧪 Testar com Postman

1. Upload: POST `http://localhost:3001/api/upload`
2. Listar: GET `http://localhost:3001/api/files`
3. Preview: GET `http://localhost:3001/api/preview/NOME_DO_ARQUIVO`

---

## 🐳 Futuro

- Upload com autenticação
- Banco de dados em nuvem (ex: PlanetScale)
- Deploy em Render ou Railway

---

Feito com 💻 por [@SeuNomeAqui]
