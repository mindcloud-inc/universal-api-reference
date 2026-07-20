# Postbode: Native API Reference

A consolidated summary of Postbode's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.postbode.nu
- **API base URL:** `https://app.postbode.nu/api`

## Authentication

### API Key

Use a Postbode API key sent in the X-Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Authorization: <apiKey>
```

[Official authentication documentation](https://api.postbode.nu)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Letter Draft](actions/create-letter-draft.md) | `POST /mailbox/:mailbox_id/letters` | [docs](https://github.com/postbode/postbode-api#send-letter) |
| [Get Letter](actions/get-letter.md) | `GET /mailbox/:mailbox_id/letter/:letter_id` | [docs](https://github.com/postbode/postbode-api#list-all-letters-in-mailbox) |
| [List Letters](actions/list-letters.md) | `GET /mailbox/:mailbox_id/letters` | [docs](https://github.com/postbode/postbode-api#list-all-letters-in-mailbox) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /mailbox` | [docs](https://github.com/postbode/postbode-api#list-all-available-mailboxes) |
| [Send Letter](actions/send-letter.md) | `POST /mailbox/:mailbox_id/letters` | [docs](https://github.com/postbode/postbode-api#send-letter) |
