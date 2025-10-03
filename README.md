# Laravel Webhooks Package

Um pacote Laravel para gerenciar **Webhooks personalizados**, permitindo que sistemas externos se integrem facilmente à sua aplicação.

## 🚀 Funcionalidades

* CRUD completo de webhooks (criar, listar, editar, deletar).
* Definição de URL de destino para disparo dos eventos.
* Suporte a eventos internos do Laravel (exemplo: criação de usuário, pedido, pagamento, etc.).
* Envio de requisições HTTP (POST) assíncronas.
* Teste de disparo de webhook diretamente pelo painel.
* Estrutura desacoplada, podendo ser usada em qualquer projeto Laravel.

---

## 📦 Instalação

Clone o repositório e instale as dependências:

```bash
git clone https://github.com/seuusuario/laravel-webhooks.git
cd laravel-webhooks
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
```

---

## ⚡ Uso

1. Acesse o painel de **Webhooks** no menu lateral.
2. Cadastre a URL de destino (por exemplo, `https://meuservico.com/webhook-receiver`).
3. Selecione o evento que deseja monitorar.
4. Teste o disparo do webhook pelo botão de **Testar Envio**.

Exemplo de payload enviado:

```json
{
  "event": "user.created",
  "timestamp": "2025-10-02T19:30:00Z",
  "data": {
    "id": 1,
    "name": "João da Silva",
    "email": "joao@example.com"
  }
}
```

---

## 🛠️ Tecnologias Utilizadas

* PHP 8+
* Laravel 12
* MySQL
* Bootstrap 5 (frontend do painel)
* FontAwesome (ícones do menu)

---

## 📂 Estrutura do Projeto

```
laravel-webhooks/
│
├── src/
│   ├── Controllers/
│   │   └── WebhookController.php
│   ├── Models/
│   │   └── Webhook.php
│   ├── Views/
│   │   └── index.blade.php
│   └── routes/web.php
│
├── database/
│   └── migrations/
│       └── create_webhooks_table.php
│
├── README.md
├── composer.json
└── LICENSE
```

---

## 📸 Demonstração

![Tela de Webhooks](docs/screenshot.png)
*(Adicione aqui um print da tela do formulário/listagem de webhooks do seu painel)*

---

## 🚀 Roadmap

* [ ] Suporte a autenticação via tokens (Bearer / API Key).
* [ ] Logs de entrega dos webhooks.
* [ ] Suporte a fila (queue) para reenvio automático em caso de falha.
* [ ] Dashboard de estatísticas.

---

## 🤝 Contribuindo

Pull requests são bem-vindos. Para mudanças maiores, abra uma issue primeiro para discutir o que você gostaria de alterar.

---

## 📜 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

## 👨‍💻 Autor

Desenvolvido por Thiago Rodrigues

