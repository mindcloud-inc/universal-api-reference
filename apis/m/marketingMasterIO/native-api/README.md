# Marketing Master IO: Native API Reference

A consolidated summary of Marketing Master IO's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developers.marketingmaster.io/
- **OpenAPI specification:** https://developers.marketingmaster.io/mmio-openapi.json
- **API base URL:** `https://api.marketingmaster.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.marketingmaster.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subscriber Tag](actions/add-subscriber-tag.md) | `POST /v1/messenger/subscriber/:subscriber_id/tags/:tag` | [docs](https://developers.marketingmaster.io/) |
| [Add Subscriber User Data](actions/add-subscriber-user-data.md) | `POST /v1/messenger/subscriber/:subscriber_id/user_data/:variable_key` | [docs](https://developers.marketingmaster.io/) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts/list` | [docs](https://developers.marketingmaster.io/) |
| [Create Contact Book](actions/create-contact-book.md) | `POST /v1/contacts/books` | [docs](https://developers.marketingmaster.io/) |
| [Create Contact Tag](actions/create-contact-tag.md) | `POST /v1/contacts/tags` | [docs](https://developers.marketingmaster.io/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/list/:contact_id` | [docs](https://developers.marketingmaster.io/) |
| [Delete Contact Book](actions/delete-contact-book.md) | `DELETE /v1/contacts/books/:book_id` | [docs](https://developers.marketingmaster.io/) |
| [Delete Contact Tag](actions/delete-contact-tag.md) | `DELETE /v1/contacts/tags/:tag` | [docs](https://developers.marketingmaster.io/) |
| [Disable Facebook Page](actions/disable-facebook-page.md) | `DELETE /v1/facebook_pages/:page_id` | [docs](https://developers.marketingmaster.io/) |
| [Enable Facebook Page](actions/enable-facebook-page.md) | `POST /v1/facebook_pages/:page_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Chat Sequence](actions/get-chat-sequence.md) | `GET /v1/messenger/chat_sequences/:chat_sequence_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Chatbot Flow](actions/get-chatbot-flow.md) | `GET /v1/messenger/flows/:flow_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/list/:contact_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Contact Book](actions/get-contact-book.md) | `GET /v1/contacts/books/:book_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Contact Tag](actions/get-contact-tag.md) | `GET /v1/contacts/tags/:tag` | [docs](https://developers.marketingmaster.io/) |
| [Get Custom Variable](actions/get-custom-variable.md) | `GET /v1/messenger/custom_variables/:variable_key` | [docs](https://developers.marketingmaster.io/) |
| [Get Facebook Page](actions/get-facebook-page.md) | `GET /v1/facebook_pages/:page_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Google Sheet](actions/get-google-sheet.md) | `GET /v1/google_sheets/:google_sheet_id` | [docs](https://developers.marketingmaster.io/) |
| [Get Messenger Subscriber](actions/get-messenger-subscriber.md) | `GET /v1/messenger/subscriber/:subscriber_id` | [docs](https://developers.marketingmaster.io/) |
| [List Chat Sequences](actions/list-chat-sequences.md) | `GET /v1/messenger/chat_sequences` | [docs](https://developers.marketingmaster.io/) |
| [List Chatbot Flows](actions/list-chatbot-flows.md) | `GET /v1/messenger/flows` | [docs](https://developers.marketingmaster.io/) |
| [List Contact Books](actions/list-contact-books.md) | `GET /v1/contacts/books` | [docs](https://developers.marketingmaster.io/) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /v1/contacts/tags` | [docs](https://developers.marketingmaster.io/) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts/list` | [docs](https://developers.marketingmaster.io/) |
| [List Custom Variables](actions/list-custom-variables.md) | `GET /v1/messenger/custom_variables` | [docs](https://developers.marketingmaster.io/) |
| [List Facebook Pages](actions/list-facebook-pages.md) | `GET /v1/facebook_pages` | [docs](https://developers.marketingmaster.io/) |
| [List Google Sheets](actions/list-google-sheets.md) | `GET /v1/google_sheets` | [docs](https://developers.marketingmaster.io/) |
| [List Messenger Subscribers](actions/list-messenger-subscribers.md) | `GET /v1/messenger/subscriber` | [docs](https://developers.marketingmaster.io/) |
| [Opt In Chat Sequence Subscriber](actions/opt-in-chat-sequence-subscriber.md) | `POST /v1/messenger/chat_sequences/:chat_sequence_id/:subscriber_id` | [docs](https://developers.marketingmaster.io/) |
| [Opt Out Chat Sequence Subscriber](actions/opt-out-chat-sequence-subscriber.md) | `DELETE /v1/messenger/chat_sequences/:chat_sequence_id/:subscriber_id` | [docs](https://developers.marketingmaster.io/) |
| [Remove Subscriber Tag](actions/remove-subscriber-tag.md) | `DELETE /v1/messenger/subscriber/:subscriber_id/tags/:tag` | [docs](https://developers.marketingmaster.io/) |
| [Remove Subscriber User Data](actions/remove-subscriber-user-data.md) | `DELETE /v1/messenger/subscriber/:subscriber_id/user_data/:variable_key` | [docs](https://developers.marketingmaster.io/) |
| [Send Custom Message](actions/send-custom-message.md) | `POST /v1/messenger/sending/:subscriber_id/custom` | [docs](https://developers.marketingmaster.io/) |
| [Send Flow Message](actions/send-flow-message.md) | `POST /v1/messenger/sending/:subscriber_id/messages/:payload_id` | [docs](https://developers.marketingmaster.io/) |
| [Update Contact](actions/update-contact.md) | `POST /v1/contacts/list/:contact_id` | [docs](https://developers.marketingmaster.io/) |
| [Update Contact Book](actions/update-contact-book.md) | `POST /v1/contacts/books/:book_id` | [docs](https://developers.marketingmaster.io/) |
| [Validate Access Token](actions/validate-access-token.md) | `GET /v1/authenticate` | [docs](https://developers.marketingmaster.io/) |
