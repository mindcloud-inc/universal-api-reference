# HTML/CSS to Image app: Native API Reference

A consolidated summary of HTML/CSS to Image app's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.htmlcsstoimage.com
- **API base URL:** `https://hcti.io`

## Authentication

### User ID + API Key

Authenticate with HTTP Basic auth. Use your HTML/CSS to Image User ID as the username and your API Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.htmlcsstoimage.com/getting-started/using-the-api/)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | `POST /v1/image` | [docs](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#creating-an-image) |
| [Create Template](actions/create-template.md) | `POST /v1/template` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#creating-a-template) |
| [Delete Image](actions/delete-image.md) | `DELETE /v1/image/:imageId` | [docs](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#deleting-an-image) |
| [Delete Images Batch](actions/delete-images-batch.md) | `DELETE /v1/image/batch` | [docs](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#batch-deletion) |
| [Get Image](actions/get-image.md) | `GET /v1/image/:imageId.:format` | [docs](https://docs.htmlcsstoimage.com/getting-started/using-the-api/#getting-an-image) |
| [Get Usage](actions/get-usage.md) | `GET /v1/usage` | [docs](https://docs.htmlcsstoimage.com/guides/advanced/account-usage/) |
| [List Template Versions](actions/list-template-versions.md) | `GET /v1/template/:templateId` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#listing-your-template-versions) |
| [List Templates](actions/list-templates.md) | `GET /v1/template` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#listing-your-templates) |
| [Render Template](actions/render-template.md) | `POST /v1/image/:templateId` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#creating-an-image-with-a-template) |
| [Render Template Version](actions/render-template-version.md) | `POST /v1/image/:templateId/:templateVersion` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#creating-an-image-with-a-template) |
| [Update Template](actions/update-template.md) | `POST /v1/template/:templateId` | [docs](https://docs.htmlcsstoimage.com/getting-started/templates/#editing-a-template) |
