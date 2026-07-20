# ChatPDF: Native API Reference

A consolidated summary of ChatPDF's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.chatpdf.com/docs/api/backend
- **API base URL:** `https://api.chatpdf.com/v1`

## Authentication

### API Key

Provide the ChatPDF API key. ChatPDF requires the key in the x-api-key request header.

### Credentials

- **API Key:** `apiKey` · required · Your ChatPDF backend API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.chatpdf.com/docs/api/backend)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add PDF From URL](actions/add-pdf-from-url.md) | `POST /sources/add-url` | [docs](https://www.chatpdf.com/docs/api/backend) |
| [Delete PDF Sources](actions/delete-pdf-sources.md) | `POST /sources/delete` | [docs](https://www.chatpdf.com/docs/api/backend) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chats/message` | [docs](https://www.chatpdf.com/docs/api/backend) |
| [Send Chat Message With References](actions/send-chat-message-with-references.md) | `POST /chats/message` | [docs](https://www.chatpdf.com/docs/api/backend) |
| [Stream Chat Message](actions/stream-chat-message.md) | `POST /chats/message` | [docs](https://www.chatpdf.com/docs/api/backend) |
| [Upload PDF File](actions/upload-pdf-file.md) | `POST /sources/add-file` | [docs](https://www.chatpdf.com/docs/api/backend) |
