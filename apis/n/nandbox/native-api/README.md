# nandbox: Native API Reference

A consolidated summary of nandbox's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developer.nandbox.com/
- **API base URL:** `{downloadServer}/`

## Authentication

### API Token

Use the nandbox authorization token from the API section of your nandbox account.

### Credentials

- **API Key:** `apiKey` · required
- **Bot URI:** `uri` · required · Full websocket URI from the nandbox quick-start config.
- **Download Server:** `downloadServer` · required · Full download base URL from the nandbox quick-start config, including the trailing slash.
- **Upload Server:** `uploadServer` · required · Full upload base URL from the nandbox quick-start config, including the trailing slash.

Send these headers with each API request:

```http
X-Token: <apiKey>
```

[Official authentication documentation](https://developer.nandbox.com/authentication)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Media File](actions/download-media-file.md) | `GET {{mediaId}}` | [docs](https://developer.nandbox.com/media/downloading-media-files) |
