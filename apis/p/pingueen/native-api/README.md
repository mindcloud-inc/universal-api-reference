# Pingueen: Native API Reference

A consolidated summary of Pingueen's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://etinet.gitbook.io/pingueen/api-reference
- **API base URL:** `https://api.pingueen.it/ext/v2/{businessname}`

## Authentication

### API Key

Connect with your Pingueen Secret Key and Business Name. Complete the Pingueen account activation wizard before using write actions, because Pingueen currently blocks mutating endpoints until activation is finished.

### Credentials

- **API Key:** `apiKey` · required
- **Business Name:** `businessName` · required · Business name from Pingueen settings; used in the API base URL.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://etinet.gitbook.io/pingueen/api-reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Client Agents](actions/assign-client-agents.md) | `POST /clients/:_id/assign-agents` | [docs](https://etinet.gitbook.io/pingueen/api-reference/clients/assign-agent-to-a-client) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://etinet.gitbook.io/pingueen/api-reference/clients/create-a-new-client) |
| [Create Template](actions/create-template.md) | `POST /user/templates` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/create-template) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/:id` | [docs](https://etinet.gitbook.io/pingueen/api-reference/clients/remove-a-client) |
| [Delete Template](actions/delete-template.md) | `DELETE /user/templates/:template_name` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/remove-template) |
| [Get User Info](actions/get-user-info.md) | `GET /me` | [docs](https://etinet.gitbook.io/pingueen/api-reference/user-info) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://etinet.gitbook.io/pingueen/api-reference/clients/retrive-a-list-of-clients) |
| [List Templates](actions/list-templates.md) | `GET /user/templates` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/templates-list) |
| [Send Interactive Message](actions/send-interactive-message.md) | `POST /messages` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/freeform-messages/interactive-messages) |
| [Send Interactive Template](actions/send-interactive-template.md) | `POST /template` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/send-templates/send-interactive-template) |
| [Send Media Message](actions/send-media-message.md) | `POST /messages` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/freeform-messages/send-media-message) |
| [Send Media Template](actions/send-media-template.md) | `POST /template` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/send-templates/send-media-template) |
| [Send Text Message](actions/send-text-message.md) | `POST /messages` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/freeform-messages/send-text-message) |
| [Send Text Template](actions/send-text-template.md) | `POST /template` | [docs](https://etinet.gitbook.io/pingueen/api-reference/messages/templates/send-templates/send-text-template) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://etinet.gitbook.io/pingueen/api-reference/clients/update-an-existing-client) |
