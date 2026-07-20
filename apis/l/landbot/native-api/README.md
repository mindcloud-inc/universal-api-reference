# Landbot: Native API Reference

A consolidated summary of Landbot's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.landbot.io
- **API base URL:** `https://api.landbot.io`

## Authentication

### API Key

Use your Landbot personal access token for Platform API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.landbot.io/article/qf1gzzgeez-how-to-generate-your-personal-access-token-and-how-to-use-it)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 0–100). Use `offset` in the query string as the record offset.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Customer](actions/archive-customer.md) | `PUT /v1/customers/:customer_id/archive/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idArchive) |
| [Assign Customer](actions/assign-customer.md) | `PUT /v1/customers/:customer_id/assign/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssign) |
| [Assign Customer to Agent](actions/assign-customer-to-agent.md) | `PUT /v1/customers/:customer_id/assign/:agent_id/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssignAgent_id) |
| [Assign Customer to Bot](actions/assign-customer-to-bot.md) | `PUT /v1/customers/:customer_id/assign_bot/:bot_id/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssign_botBot_id) |
| [Block Customer](actions/block-customer.md) | `PUT /v1/customers/:customer_id/block/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idBlock) |
| [Create Customer Field](actions/create-customer-field.md) | `POST /v1/customers/:customer_id/fields/:field_name/` | [docs](https://api.landbot.io/#api-CustomerFields-CreateField) |
| [Create Message Hook](actions/create-message-hook.md) | `POST /v1/channels/:channel_id/message_hooks/` | [docs](https://api.landbot.io/#api-MessageHooks-PostHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooks) |
| [Delete Message Hook](actions/delete-message-hook.md) | `DELETE /v1/channels/:channel_id/message_hooks/:hook_id/` | [docs](https://api.landbot.io/#api-MessageHooks-DeleteHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooksHook_id) |
| [Get Channel](actions/get-channel.md) | `GET /v1/channels/:channel_id/` | [docs](https://api.landbot.io/#api-Channels-GetHttpsApiLandbotIoV1ChannelsChannel_id) |
| [Get Customer](actions/get-customer.md) | `GET /v1/customers/:customer_id/` | [docs](https://api.landbot.io/#api-Customers-GetHttpsApiLandbotIoV1CustomersCustomer_id) |
| [Get Customer Field](actions/get-customer-field.md) | `GET /v1/customers/:customer_id/fields/:field_name/` | [docs](https://api.landbot.io/#api-CustomerFields-GetHttpsApiLandbotIoV1CustomersCustomer_idFieldsField_name) |
| [Get Message Hook](actions/get-message-hook.md) | `GET /v1/channels/:channel_id/message_hooks/:hook_id/` | [docs](https://api.landbot.io/#api-MessageHooks-GetHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooksHook_id) |
| [List Channels](actions/list-channels.md) | `GET /v1/channels/` | [docs](https://api.landbot.io/#api-Channels-GetHttpsApiLandbotIoV1Channels) |
| [List Customers](actions/list-customers.md) | `GET /v1/customers/` | [docs](https://api.landbot.io/#api-Customers-GetHttpsApiLandbotIoV1Customers) |
| [List Message Hooks](actions/list-message-hooks.md) | `GET /v1/channels/:channel_id/message_hooks/` | [docs](https://api.landbot.io/#api-MessageHooks-GetHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooks) |
| [List WhatsApp Templates](actions/list-whatsapp-templates.md) | `GET /v1/channels/whatsapp/templates/` | [docs](https://api.landbot.io/#api-WhatsApp_templates-GetHttpsApiLandbotIoV1ChannelsWhatsappTemplates) |
| [Unarchive Customer](actions/unarchive-customer.md) | `PUT /v1/customers/:customer_id/unarchive/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idUnarchive) |
| [Unassign Customer](actions/unassign-customer.md) | `PUT /v1/customers/:customer_id/unassign/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idUnassign) |
| [Unblock Customer](actions/unblock-customer.md) | `PUT /v1/customers/:customer_id/unblock/` | [docs](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idUnblock) |
| [Update Customer Field](actions/update-customer-field.md) | `PUT /v1/customers/:customer_id/fields/:field_name/` | [docs](https://api.landbot.io/#api-CustomerFields-ChangeField) |
