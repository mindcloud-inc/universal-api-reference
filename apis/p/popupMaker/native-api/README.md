# Popup Maker: Native API Reference

A consolidated summary of Popup Maker's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.popupmaker.com/
- **API base URL:** `https://popupmaker.com/`

## Authentication

### API Key

Use the account API key from Popup Maker Settings. The verified connection flow also requires a fixed request body field `appname=Wordpress`, based on the official WordPress plugin.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.popupmaker.com/en/article/how-to-get-the-popup-maker-api-key-140rk9g/)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connect Account and List Popups](actions/connect-account-and-list-popups.md) | `POST app/connect` | [docs](https://help.popupmaker.com/en/article/how-to-use-the-popup-maker-plugin-in-wordpress-gnf4a7/) |
