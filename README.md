# 🚀 API de Produtos RESTful - Refatoração e Boas Práticas

Este projeto foi desenvolvido como parte da **Aula 07** do curso de Análise e Desenvolvimento de Sistemas. O objetivo principal foi realizar a manutenção e refatoração de uma API de gerenciamento de produtos que não seguia as convenções da arquitetura REST.

## 📋 Sobre o Projeto

A API original apresentava problemas como o uso de verbos nas URLs, métodos HTTP inadequados e falta de códigos de status semânticos. Nesta versão refatorada, apliquei os padrões de mercado para garantir uma integração mais simples e uma manutenção robusta.

### Principais Melhorias:
- **Padronização de URIs:** Remoção de verbos (ex: de `/listarProdutos` para `/produtos`).
- **Uso correto de Métodos HTTP:** Aplicação de `GET`, `POST`, `PUT`, `PATCH` e `DELETE`.
- **Status Codes Semânticos:** Implementação de retornos como `201 Created`, `204 No Content`, `400 Bad Request` e `404 Not Found`.
- **Middleware de Log:** Registro em tempo real de todas as requisições no terminal.
- **Validação de Dados:** Proteção contra entradas inválidas (ex: preço zerado ou ausência de nome).

---

## 🛠️ Tecnologias
- **Node.js** (Ambiente de execução)
- **Express** (Framework Web)
- **Postman** (Testes de API)

---

## ⚙️ Como executar o projeto

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git](https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git)
2. Instale as dependências:
```Bash
   npm install
```
3.Inicie o servidor (Modo Watch):
```Bash
node --watch server-restful.js
```
O servidor estará rodando em: http://localhost:3000

## 📡 Guia de Testes (Endpoints)
Método,Endpoint,Descrição,Status Sucesso
GET    /produtos,Lista todos os produtos cadastrados.,200 OK
GET    /produtos/:id,Busca um produto específico pelo ID.,200 OK
POST   /produtos,Adiciona um novo produto (Requer Body JSON).,201 Created
PUT    /produtos/:id,Atualiza todos os dados de um produto.,200 OK
PATCH  /produtos/:id,Atualização parcial (ex: apenas o preço).,200 OK
DELETE /produtos/:id,Remove um produto do sistema.,204 No Content

Exemplo de Body para POST/PUT:
```
{
  "nome": "Teclado Mecânico",
  "preco": 450.00,
  "estoque": 15,
  "categoria": "Periféricos"
}
```

## 🧪 Testando com Postman
Para realizar os testes conforme os critérios da atividade:
1. Abra o Postman.
2.Configure o método e a URL desejada.
3.Nas requisições POST, PUT e PATCH, vá na aba Body, selecione raw e mude o tipo para JSON para colar os dados.
4.Clique em Send e verifique o Status Code no canto inferior direito.

## 📝 Autor
Desenvolvido como atividade prática do curso ITEAM de Desenvolvimento FULLSTACK.
Rodrigo Matos Gomes
