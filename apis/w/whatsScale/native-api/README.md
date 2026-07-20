# WhatsScale: Native API Reference

A consolidated summary of WhatsScale's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://whatsscale.com/docs
- **OpenAPI specification:** https://whatsscale.com/api-docs
- **API base URL:** `https://proxy.whatsscale.com`

## Authentication

### API Key

Use a WhatsScale API key. Requests send the key in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required · WhatsScale API key. Runtime requests send this value as the X-Api-Key header.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://whatsscale.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `equals`.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag to CRM Contact](actions/add-tag-to-crm-contact.md) | `POST /api/crm/contacts/:id/tags` | [docs](https://whatsscale.com/docs) |
| [Check Job Status](actions/check-job-status.md) | `GET /api/status/:jobId` | [docs](https://whatsscale.com/docs) |
| [Check WhatsApp Number](actions/check-whats-app-number.md) | `POST /api/checkWhatsapp` | [docs](https://whatsscale.com/docs) |
| [Create CRM Contact](actions/create-crm-contact.md) | `POST /api/crm/contacts` | [docs](https://whatsscale.com/docs) |
| [Delete CRM Contact](actions/delete-crm-contact.md) | `DELETE /api/crm/contacts/:id` | [docs](https://whatsscale.com/docs) |
| [Find CRM Contact by Phone](actions/find-crm-contact-by-phone.md) | `GET /api/crm/contacts/phone/:phone` | [docs](https://whatsscale.com/docs) |
| [Get CRM Contact](actions/get-crm-contact.md) | `GET /api/crm/contacts/:id` | [docs](https://whatsscale.com/docs) |
| [List CRM Contacts](actions/list-crm-contacts.md) | `GET /api/crm/contacts` | [docs](https://whatsscale.com/docs) |
| [List CRM Tags](actions/list-crm-tags.md) | `GET /api/crm/tags` | [docs](https://whatsscale.com/docs) |
| [List Sessions](actions/list-sessions.md) | `GET /api/sessions` | [docs](https://whatsscale.com/docs) |
| [List WhatsApp Contacts](actions/list-whats-app-contacts.md) | `GET /api/:session/contacts` | [docs](https://whatsscale.com/docs) |
| [List WhatsApp Groups](actions/list-whats-app-groups.md) | `GET /api/:session/groups` | [docs](https://whatsscale.com/docs) |
| [Post Image Story](actions/post-image-story.md) | `POST /api/status/image` | [docs](https://whatsscale.com/docs) |
| [Post Text Story](actions/post-text-story.md) | `POST /api/status/text` | [docs](https://whatsscale.com/docs) |
| [Post Video Story](actions/post-video-story.md) | `POST /api/status/video` | [docs](https://whatsscale.com/docs) |
| [Remove Tag from CRM Contact](actions/remove-tag-from-crm-contact.md) | `DELETE /api/crm/contacts/:id/tags/:tag` | [docs](https://whatsscale.com/docs) |
| [Send Document](actions/send-document.md) | `POST /api/sendDocument` | [docs](https://whatsscale.com/docs) |
| [Send Image](actions/send-image.md) | `POST /api/sendImage` | [docs](https://whatsscale.com/docs) |
| [Send Location](actions/send-location.md) | `POST /api/sendLocation` | [docs](https://whatsscale.com/docs) |
| [Send Poll](actions/send-poll.md) | `POST /api/sendPoll` | [docs](https://whatsscale.com/docs) |
| [Send Text Message](actions/send-text-message.md) | `POST /api/sendText` | [docs](https://whatsscale.com/docs) |
| [Send Video](actions/send-video.md) | `POST /api/sendVideo` | [docs](https://whatsscale.com/docs) |
| [Test Authentication](actions/test-authentication.md) | `GET /api/auth/test` | [docs](https://whatsscale.com/docs) |
| [Update CRM Contact](actions/update-crm-contact.md) | `PATCH /api/crm/contacts/:id` | [docs](https://whatsscale.com/docs) |
