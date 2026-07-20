# Realcrux: Native API Reference

A consolidated summary of Realcrux's API configuration and 5 documented operations.

- **API base URL:** `https://sendcrux.com/api/v1`

## Authentication

### API Token

Connect Realcrux with the API token from your Sendcrux Account > API page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sendcrux.com/wordpressPage)

## Endpoints (5 documented)

| Operation | Method & path |
| --- | --- |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE subscribers/:uid` |
| [Find Subscriber By Email](actions/find-subscriber-by-email.md) | `GET subscribers/email/:email` |
| [Get Mail List](actions/get-mail-list.md) | `GET lists/:uid` |
| [List Mail Lists](actions/list-mail-lists.md) | `GET lists` |
| [Upsert Subscriber](actions/upsert-subscriber.md) | `POST subscribers` |
