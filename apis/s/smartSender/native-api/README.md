# Smart Sender: Native API Reference

A consolidated summary of Smart Sender's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1705902128/API-kuvaus
- **API base URL:** `https://api.smartsender.com`

## Authentication

### API Key

Use a Smart Sender project API token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676673382/API%2Bintegration%2B-%2Ben)

## API conventions

Responses from this API use JSON. Response data is read from `collection`. The total page count is read from `cursor.pages`. The current page number is read from `cursor.page`.

## Pagination

Use `limitation` in the query string to set the page size (default 20; accepted range 1–20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Funnel](actions/add-contact-funnel.md) | `POST /v1/contacts/:contactId/funnels/:serviceKey` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben) |
| [Add Contact Tag](actions/add-contact-tag.md) | `POST /v1/contacts/:contactId/tags/:tagId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97386531/Contact%2BTags%2BAPI) |
| [Assign Chat](actions/assign-chat.md) | `POST /v1/chats/:chatId/forward/:operatorId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben) |
| [Close Chat](actions/close-chat.md) | `PUT /v1/chats/:chatId/close` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben) |
| [Create Channel Gate](actions/create-channel-gate.md) | `POST /v1/channels/:channelId/gates` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben) |
| [Create Product](actions/create-product.md) | `POST /v1/products` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432) |
| [Create Variable](actions/create-variable.md) | `POST /v1/variables` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben) |
| [Delete Product](actions/delete-product.md) | `DELETE /v1/products/:productId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432) |
| [Delete Variable](actions/delete-variable.md) | `DELETE /v1/variables/:variableId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben) |
| [Fire Contact Event](actions/fire-contact-event.md) | `POST /v1/contacts/:contactId/fire` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Get Channel](actions/get-channel.md) | `GET /v1/channels/:channelId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben) |
| [Get Chat](actions/get-chat.md) | `GET /v1/chats/:chatId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:contactId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Get Contact Chat](actions/get-contact-chat.md) | `GET /v1/contacts/:contactId/chat` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Get Contact Gates](actions/get-contact-gates.md) | `GET /v1/contacts/:contactId/gates` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Get Contact Info](actions/get-contact-info.md) | `GET /v1/contacts/:contactId/info` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [List Channels](actions/list-channels.md) | `GET /v1/channels` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /v1/chats/:chatId/messages` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben) |
| [List Chats](actions/list-chats.md) | `GET /v1/chats` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben) |
| [List Contact Funnels](actions/list-contact-funnels.md) | `GET /v1/contacts/:contactId/funnels` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben) |
| [List Contact Messages](actions/list-contact-messages.md) | `GET /v1/contacts/:contactId/messages` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /v1/contacts/:contactId/tags` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97386531/Contact%2BTags%2BAPI) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [List Products](actions/list-products.md) | `GET /v1/products` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432) |
| [List Variables](actions/list-variables.md) | `GET /v1/variables` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben) |
| [Mark Chat Read](actions/mark-chat-read.md) | `PUT /v1/chats/:chatId/read` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676542648/Chats%2BAPI%2B-%2Ben) |
| [Merge Contacts](actions/merge-contacts.md) | `POST /v1/contacts/:contactId/unite/:targetContactId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Remove Contact Funnel](actions/remove-contact-funnel.md) | `DELETE /v1/contacts/:contactId/funnels/:serviceKey` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444426/Contact%2BFunnels%2BAPI%2B-%2Ben) |
| [Remove Contact Tag](actions/remove-contact-tag.md) | `DELETE /v1/contacts/:contactId/tags/:tagId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97386531/Contact%2BTags%2BAPI) |
| [Search Contacts](actions/search-contacts.md) | `GET /v1/contacts/search` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Send Message](actions/send-message.md) | `POST /v1/contacts/:contactId/send` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben) |
| [Update Channel](actions/update-channel.md) | `PUT /v1/channels/:channelId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contacts/:contactId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444281/Contacts%2BAPI%2B-%2Ben) |
| [Update Product](actions/update-product.md) | `PUT /v1/products/:productId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/97255432) |
| [Update Variable](actions/update-variable.md) | `PUT /v1/variables/:variableId` | [docs](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575629/Variables%2BAPI%2B-%2Ben) |
