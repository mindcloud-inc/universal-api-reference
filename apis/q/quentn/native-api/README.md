# Quentn: Native API Reference

A consolidated summary of Quentn's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://help.quentn.com/hc/en-150/sections/4517317189009-API-documentation
- **OpenAPI specification:** https://app.swaggerhub.com/apis/info_quentn.com/Quentn-Official-API/1.0.0
- **API base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`

## Authentication

### API Key

Connect Quentn with a standard API key. The app uses the configured Quentn base URL and the saved API key credential for authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.quentn.com/hc/en-150/articles/4469776028561-Create-API-key)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Comment](actions/add-contact-comment.md) | `POST /contact/:contact_id/comments` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [Add Contact to Campaign](actions/add-contact-to-campaign.md) | `POST /cb/:cb_id` | [docs](https://help.quentn.com/hc/en-150/articles/4518054010129-Campaign-API) |
| [Create Contact](actions/create-contact.md) | `POST /contact` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /custom-fields` | [docs](https://help.quentn.com/hc/en-150/articles/4518070370577-Custom-fields-API) |
| [Create Email](actions/create-email.md) | `POST /mail/add` | [docs](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API) |
| [Create Term](actions/create-term.md) | `POST /terms` | [docs](https://help.quentn.com/hc/en-150/articles/4518012188945-Terms-API) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:contact_id` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [List Contact Comments](actions/list-contact-comments.md) | `GET /contact/:contact_id/comments` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [List Contact Terms](actions/list-contact-terms.md) | `GET /contact/:contact_id/terms` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://help.quentn.com/hc/en-150/articles/4518070370577-Custom-fields-API) |
| [List Mail Senders](actions/list-mail-senders.md) | `GET /mail/senders` | [docs](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API) |
| [List Terms](actions/list-terms.md) | `GET /terms` | [docs](https://help.quentn.com/hc/en-150/articles/4518012188945-Terms-API) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://help.quentn.com/hc/en-150/articles/19990855749265-User-API) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contact/:contact_id` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [Retrieve Contacts by Mail](actions/retrieve-contacts-by-mail.md) | `GET /contact/:contact_mail` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [Retrieve Custom Field by ID](actions/retrieve-custom-field-by-id.md) | `GET /custom-fields/:field_id` | [docs](https://help.quentn.com/hc/en-150/articles/4518070370577-Custom-fields-API) |
| [Retrieve Email](actions/retrieve-email.md) | `GET /mail/:email_id` | [docs](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API) |
| [Retrieve Term by ID](actions/retrieve-term-by-id.md) | `GET /terms/:term_id` | [docs](https://help.quentn.com/hc/en-150/articles/4518012188945-Terms-API) |
| [Send Email](actions/send-email.md) | `POST /mail/:email_id/send` | [docs](https://help.quentn.com/hc/en-150/articles/4518209942289-Mail-API) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:contact_id` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
| [Update Contact Comment](actions/update-contact-comment.md) | `PUT /contact/:contact_id/comments` | [docs](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API) |
