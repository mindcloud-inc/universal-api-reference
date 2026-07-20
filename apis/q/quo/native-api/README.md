# Quo: Native API Reference

A consolidated summary of Quo's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://www.quo.com/docs/mdx/api-reference/introduction
- **API base URL:** `https://api.openphone.com/v1`

## Authentication

### API Token

Use a Quo API token from account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.quo.co/docs/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `maxResults` in the query string to set the page size (default 10; accepted range 1–50). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Call Summary Webhook](actions/create-call-summary-webhook.md) | `POST /webhooks/call-summaries` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-call-summaries) |
| [Create Call Transcript Webhook](actions/create-call-transcript-webhook.md) | `POST /webhooks/call-transcripts` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-call-transcripts) |
| [Create Call Webhook](actions/create-call-webhook.md) | `POST /webhooks/calls` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-calls) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://www.quo.com/docs/mdx/api-reference/contacts/create-a-contact) |
| [Create Message Webhook](actions/create-message-webhook.md) | `POST /webhooks/messages` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/create-a-new-webhook-for-messages) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/contacts/delete-a-contact) |
| [Delete Webhook By ID](actions/delete-webhook-by-id.md) | `DELETE /webhooks/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/delete-a-webhook-by-id) |
| [Get Call By ID](actions/get-call-by-id.md) | `GET /calls/:callId` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/get-a-call-by-id) |
| [Get Call Recordings](actions/get-call-recordings.md) | `GET /call-recordings/:callId` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/get-recordings-for-a-call) |
| [Get Call Summary](actions/get-call-summary.md) | `GET /call-summaries/:callId` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/get-a-summary-for-a-call) |
| [Get Call Transcript](actions/get-call-transcript.md) | `GET /call-transcripts/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/get-a-transcription-for-a-call) |
| [Get Call Voicemail](actions/get-call-voicemail.md) | `GET /call-voicemails/:callId` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/get-a-voicemail-for-a-call) |
| [Get Contact By ID](actions/get-contact-by-id.md) | `GET /contacts/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/contacts/get-a-contact-by-id) |
| [Get Contact Custom Fields](actions/get-contact-custom-fields.md) | `GET /contact-custom-fields` | [docs](https://www.quo.com/docs/mdx/api-reference/contact-custom-fields/get-contact-custom-fields) |
| [Get Message By ID](actions/get-message-by-id.md) | `GET /messages/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/messages/get-a-message-by-id) |
| [Get Phone Number By ID](actions/get-phone-number-by-id.md) | `GET /phone-numbers/:phoneNumberId` | [docs](https://www.quo.com/docs/mdx/api-reference/phone-numbers/get-a-phone-number-by-id) |
| [Get User By ID](actions/get-user-by-id.md) | `GET /users/:userId` | [docs](https://www.quo.com/docs/mdx/api-reference/users/get-a-user-by-id) |
| [Get Webhook By ID](actions/get-webhook-by-id.md) | `GET /webhooks/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/get-a-webhook-by-id) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://www.quo.com/docs/mdx/api-reference/calls/list-calls) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.quo.com/docs/mdx/api-reference/contacts/list-contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://www.quo.com/docs/mdx/api-reference/conversations/list-conversations) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://www.quo.com/docs/mdx/api-reference/messages/list-messages) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /phone-numbers` | [docs](https://www.quo.com/docs/mdx/api-reference/phone-numbers/list-phone-numbers) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.quo.com/docs/mdx/api-reference/users/list-users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.quo.com/docs/mdx/api-reference/webhooks/lists-all-webhooks) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://www.quo.com/docs/mdx/api-reference/messages/send-a-text-message) |
| [Update Contact By ID](actions/update-contact-by-id.md) | `PATCH /contacts/:id` | [docs](https://www.quo.com/docs/mdx/api-reference/contacts/update-a-contact-by-id) |
