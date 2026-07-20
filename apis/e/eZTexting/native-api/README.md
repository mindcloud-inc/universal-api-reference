# EZ Texting: Native API Reference

A consolidated summary of EZ Texting's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.eztexting.com/docs/getting-started
- **API base URL:** `https://a.eztexting.com/v1`

## Authentication

### Token Credentials

Connect EZ Texting using your EZ Texting username and password. MindCloud exchanges them for a Bearer access token through EZ Texting's token endpoints.

### Credentials

- **Username:** `username` · required · Your EZ Texting account username or email address.
- **Password:** `password` · required · Your EZ Texting account password.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://a.eztexting.com/v1/tokens/create.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://a.eztexting.com/v1/tokens/refresh. A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.eztexting.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `totalPages`. The current page number is read from `number`.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts to Contact Group](actions/add-contacts-to-contact-group.md) | `POST /contact-groups/:id/contacts` | [docs](https://developers.eztexting.com/reference/contactsadd-1) |
| [Create Contact Group](actions/create-contact-group.md) | `POST /contact-groups` | [docs](https://developers.eztexting.com/reference/create_1-1) |
| [Create Media File](actions/create-media-file.md) | `POST /media-files` | [docs](https://developers.eztexting.com/reference/create_2-1) |
| [Create Message](actions/create-message.md) | `POST /messages` | [docs](https://developers.eztexting.com/reference/create_3-1) |
| [Create or Update a Batch of Contacts](actions/create-or-update-a-batch-of-contacts.md) | `POST /contacts/batch` | [docs](https://developers.eztexting.com/reference/createorupdatebatch-1) |
| [Create or Update Contact](actions/create-or-update-contact.md) | `POST /contacts` | [docs](https://developers.eztexting.com/reference/createorupdate-1) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/subscriptions` | [docs](https://developers.eztexting.com/reference/create_6-1) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:phoneNumber` | [docs](https://developers.eztexting.com/reference/delete-1) |
| [Delete Contact Group](actions/delete-contact-group.md) | `DELETE /contact-groups/:id` | [docs](https://developers.eztexting.com/reference/delete_2-1) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/subscriptions/:id` | [docs](https://developers.eztexting.com/reference/delete_6-1) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:phoneNumber` | [docs](https://developers.eztexting.com/reference/get-1) |
| [Get Contact Group](actions/get-contact-group.md) | `GET /contact-groups/:id` | [docs](https://developers.eztexting.com/reference/get_1-1) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /credits` | [docs](https://developers.eztexting.com/reference/creditbalance-1) |
| [Get Media File](actions/get-media-file.md) | `GET /media-files/:id` | [docs](https://developers.eztexting.com/reference/get_3-1) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /contact-groups` | [docs](https://developers.eztexting.com/reference/list_2-1) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.eztexting.com/reference/list-1) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developers.eztexting.com/reference/list_3-1) |
| [List Media Files](actions/list-media-files.md) | `GET /media-files` | [docs](https://developers.eztexting.com/reference/list_5-1) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://developers.eztexting.com/reference/list_6-1) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/subscriptions` | [docs](https://developers.eztexting.com/reference/list_8-1) |
| [Remove Contacts from Contact Group](actions/remove-contacts-from-contact-group.md) | `DELETE /contact-groups/:id/contacts` | [docs](https://developers.eztexting.com/reference/contactsremove-1) |
| [Update Contact Group](actions/update-contact-group.md) | `PUT /contact-groups/:id` | [docs](https://developers.eztexting.com/reference/update_1-1) |
