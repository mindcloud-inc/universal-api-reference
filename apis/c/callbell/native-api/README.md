# Callbell: Native API Reference

A consolidated summary of Callbell's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.callbell.eu/api/reference/introduction/
- **API base URL:** `https://api.callbell.eu/v1`

## Authentication

### API Key

Use a Callbell API key sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.callbell.eu/api/getting_started/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `meta.pages`. The current page number is read from `meta.page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Contact Conversation](actions/close-contact-conversation.md) | `POST /contacts/:uuid/conversation/close` | [docs](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_close/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.callbell.eu/api/reference/contacts_api/post_contacts/) |
| [Create Contact Note](actions/create-contact-note.md) | `POST /contacts/:uuid/conversation/note` | [docs](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_create_note/) |
| [Create Custom Status](actions/create-custom-status.md) | `POST /custom_statuses` | [docs](https://docs.callbell.eu/api/reference/custom_status_api/post_custom_status/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:uuid` | [docs](https://docs.callbell.eu/api/reference/contacts_api/delete_contact/) |
| [Delete Custom Status](actions/delete-custom-status.md) | `DELETE /custom_statuses/:uuid` | [docs](https://docs.callbell.eu/api/reference/custom_status_api/delete_custom_status/) |
| [Get Auth Me](actions/get-auth-me.md) | `GET /auth/me` | [docs](https://docs.callbell.eu/api/reference/auth_api/me/) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:uuid` | [docs](https://docs.callbell.eu/api/reference/channels_api/get_channel/) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:uuid` | [docs](https://docs.callbell.eu/api/reference/contacts_api/get_contact/) |
| [Get Contact By Phone](actions/get-contact-by-phone.md) | `GET /contacts/phone/:number` | [docs](https://docs.callbell.eu/api/reference/contacts_api/get_contact_by_phone/) |
| [Get Message Status](actions/get-message-status.md) | `GET /messages/status/:uuid` | [docs](https://docs.callbell.eu/api/reference/messages_api/get_message_status/) |
| [Get Plan](actions/get-plan.md) | `GET /plan` | [docs](https://docs.callbell.eu/api/reference/plan_api/get_plan/) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://docs.callbell.eu/api/reference/channels_api/get_channels/) |
| [List Contact Messages](actions/list-contact-messages.md) | `GET /contacts/:uuid/messages` | [docs](https://docs.callbell.eu/api/reference/contacts_api/get_contact_messages/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.callbell.eu/api/reference/contacts_api/get_contacts/) |
| [List Custom Statuses](actions/list-custom-statuses.md) | `GET /custom_statuses` | [docs](https://docs.callbell.eu/api/reference/custom_status_api/get_custom_statuses/) |
| [List Funnels](actions/list-funnels.md) | `GET /funnels` | [docs](https://docs.callbell.eu/api/reference/funnels_api/get_funnels/) |
| [Open Contact Conversation](actions/open-contact-conversation.md) | `POST /contacts/:uuid/conversation/open` | [docs](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_open/) |
| [Send Message](actions/send-message.md) | `POST /messages/send` | [docs](https://docs.callbell.eu/api/reference/messages_api/post_send_messages/) |
| [Update Channel](actions/update-channel.md) | `PATCH /channels/:uuid` | [docs](https://docs.callbell.eu/api/reference/channels_api/patch_channel/) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:uuid` | [docs](https://docs.callbell.eu/api/reference/contacts_api/patch_contacts/) |
| [Update Custom Status](actions/update-custom-status.md) | `PUT /custom_statuses/:uuid` | [docs](https://docs.callbell.eu/api/reference/custom_status_api/put_custom_status/) |
