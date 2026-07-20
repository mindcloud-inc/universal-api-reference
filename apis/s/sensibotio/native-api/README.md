# Sensibot.io: Native API Reference

A consolidated summary of Sensibot.io's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://api.sensibot.io/
- **API base URL:** `https://api.sensibot.io`

## Authentication

### API Token

Use your Sensibot API token as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.sensibot.io/)

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [All Chat History](actions/all-chat-history.md) | `POST /assistant/allchathistory` | [docs](https://api.sensibot.io/) |
| [Assistant Bot Type](actions/assistant-bot-type.md) | `POST /assistant/bot_type` | [docs](https://api.sensibot.io/) |
| [Assistant Welcome Message](actions/assistant-welcome-message.md) | `POST /assistant/welcome_message` | [docs](https://api.sensibot.io/) |
| [Chat History](actions/chat-history.md) | `POST /assistant/chathistory` | [docs](https://api.sensibot.io/) |
| [Create Customer List](actions/create-customer-list.md) | `POST /whatsappcloud/create_customerlist` | [docs](https://api.sensibot.io/) |
| [Customer List](actions/customer-list.md) | `GET /whatsappcloud/customerlist` | [docs](https://api.sensibot.io/) |
| [Get Assistant](actions/get-assistant.md) | `GET /assistant` | [docs](https://api.sensibot.io/) |
| [Human Takeover](actions/human-takeover.md) | `POST /assistant/human_takeover` | [docs](https://api.sensibot.io/) |
| [Subscriber Info](actions/subscriber-info.md) | `POST /assistant/subscriber_info` | [docs](https://api.sensibot.io/) |
| [Subscriber Variables](actions/subscriber-variables.md) | `POST /assistant/get_variables/:subscriber` | [docs](https://api.sensibot.io/) |
| [WhatsApp beta Send Chat](actions/whats-app-beta-send-chat.md) | `POST /whatsappbeta/send` | [docs](https://api.sensibot.io/) |
| [WhatsApp beta Send Chat [GET]](actions/whats-app-beta-send-chat-get.md) | `GET /whatsappbeta/send_get` | [docs](https://api.sensibot.io/) |
| [WhatsApp Bot Status](actions/whats-app-bot-status.md) | `POST /whatsappbeta/bot_status` | [docs](https://api.sensibot.io/) |
| [WhatsApp Cloud Bot Status](actions/whats-app-cloud-bot-status.md) | `POST /whatsappcloud/bot_status` | [docs](https://api.sensibot.io/) |
| [WhatsApp Cloud Send Message](actions/whats-app-cloud-send-message.md) | `POST /whatsappcloud/send` | [docs](https://api.sensibot.io/) |
| [WhatsApp Cloud Template Send Message](actions/whats-app-cloud-template-send-message.md) | `POST /whatsappcloud/send_template` | [docs](https://api.sensibot.io/) |
