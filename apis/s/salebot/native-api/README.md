# Salebot: Native API Reference

A consolidated summary of Salebot's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.salebot.pro/rabota-s-api/api-konstruktora
- **API base URL:** `https://chatter.salebot.pro/api/{apiKey}`

## Authentication

### API Key

Connect Salebot with a generated project API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Message History](actions/clear-message-history.md) | `GET /clear_history` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Create Order](actions/create-order.md) | `POST /create_order` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find All Client IDs by Variable](actions/find-all-client-ids-by-variable.md) | `GET /find_all_client_id_by_var` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find Client ID by Variable](actions/find-client-id-by-variable.md) | `GET /find_client_id_by_var` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find Client IDs by Platform ID](actions/find-client-ids-by-platform-id.md) | `POST /find_client_id_by_platform_id` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find Client IDs by Several Variables](actions/find-client-ids-by-several-variables.md) | `GET /find_all_client_id_by_several_vars` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find Clients](actions/find-clients.md) | `POST /find_clients` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Find Latest Client ID by Variable](actions/find-latest-client-id-by-variable.md) | `GET /find_latest_client_id_by_var` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Get Current Order ID](actions/get-current-order-id.md) | `GET /get_current_order_id` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Get Message History](actions/get-message-history.md) | `GET /get_history` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Get Order State](actions/get-order-state.md) | `GET /get_order_state` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Get Order Variables](actions/get-order-variables.md) | `POST /get_order_vars` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Get Variables](actions/get-variables.md) | `GET /get_variables` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [List Bot Messages](actions/list-bot-messages.md) | `GET /get_messages` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [List Clients](actions/list-clients.md) | `GET /get_clients` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [List Connected Channels](actions/list-connected-channels.md) | `GET /connected_channels` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [List Orders](actions/list-orders.md) | `GET /get_orders` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Move Order to Next State](actions/move-order-to-next-state.md) | `POST /move_order_to_next_state` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Resolve Online Chat Client](actions/resolve-online-chat-client.md) | `GET /online_chat_client_id` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Save Variables](actions/save-variables.md) | `POST /save_variables` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Send Broadcast](actions/send-broadcast.md) | `POST /broadcast` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Send Callback by Platform ID](actions/send-callback-by-platform-id.md) | `POST /send_callback_by_platform_id` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Send Message](actions/send-message.md) | `POST /message` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Set Order Variables](actions/set-order-variables.md) | `POST /set_order_vars` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Trigger Callback](actions/trigger-callback.md) | `POST /callback` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
| [Trigger Email Callback](actions/trigger-email-callback.md) | `POST /email_callback` | [docs](https://docs.salebot.pro/rabota-s-api/api-konstruktora) |
