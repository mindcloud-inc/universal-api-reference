# Bannertize: Native API Reference

A consolidated summary of Bannertize's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.bannertize.com/
- **API base URL:** `https://api.bannertize.com/v1`

## Authentication

### API Key

Connect with your Bannertize API key. Bannertize expects Authorization: Bearer <API_KEY> on every API request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.bannertize.com/)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | `POST image` | [docs](https://docs.bannertize.com/) |
| [Generate Images via Set](actions/generate-images-via-set.md) | `POST set` | [docs](https://docs.bannertize.com/) |
| [Get Account](actions/get-account.md) | `GET account` | [docs](https://docs.bannertize.com/) |
| [Get Current User](actions/get-current-user.md) | `GET user` | [docs](https://docs.bannertize.com/) |
| [Get Template](actions/get-template.md) | `GET template/:template_uid` | [docs](https://docs.bannertize.com/) |
| [Retrieve Image](actions/retrieve-image.md) | `GET image/:image_uid` | [docs](https://docs.bannertize.com/) |
| [Retrieve Set](actions/retrieve-set.md) | `GET set/:set_uid` | [docs](https://docs.bannertize.com/) |
