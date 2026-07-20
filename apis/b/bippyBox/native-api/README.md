# BippyBox: Native API Reference

A consolidated summary of BippyBox's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://bippybox.io/docs/
- **API base URL:** `https://app.bippybox.io`

## Authentication

### UID Header

Use your BippyBox UID as the API key credential. Requests to app.bippybox.io send it in the x-uid header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-uid: <apiKey>
```

[Official authentication documentation](https://bippybox.io/docs/)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Data](actions/get-user-data.md) | `GET /getuserdata` | [docs](https://bippybox.io/docs/#apikey) |
| [Trigger BippyBox](actions/trigger-bippybox.md) | `POST https://mqtt.bippybox.io/send` | [docs](https://bippybox.io/docs/#apikey) |
