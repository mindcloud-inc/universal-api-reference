# Formstack Documents: Native API Reference

A consolidated summary of Formstack Documents's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.webmerge.me/developers
- **API base URL:** `https://www.webmerge.me/api`

## Authentication

### API Key and Secret

Connect with your Formstack Documents API Key and API Secret.

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

[Official authentication documentation](https://www.webmerge.me/developers/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Combine Files](actions/combine-files.md) | `POST /tools/combine` | [docs](https://www.webmerge.me/developers/tools) |
| [Compress PDF](actions/compress-pdf.md) | `POST /tools/compress_pdf` | [docs](https://www.webmerge.me/developers/tools) |
| [Convert File to PDF](actions/convert-file-to-pdf.md) | `POST /tools/convert_to_pdf` | [docs](https://www.webmerge.me/developers/tools) |
| [Copy Document](actions/copy-document.md) | `POST /documents/:id/copy` | [docs](https://www.webmerge.me/developers/documents) |
| [Create Data Route](actions/create-data-route.md) | `POST /routes` | [docs](https://www.webmerge.me/developers/routes) |
| [Create Data Route Delivery](actions/create-data-route-delivery.md) | `POST /routes/:id/deliveries` | [docs](https://www.webmerge.me/developers/routes) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://www.webmerge.me/developers/documents) |
| [Create Document Delivery](actions/create-document-delivery.md) | `POST /documents/:id/deliveries` | [docs](https://www.webmerge.me/developers/documents) |
| [Delete Data Route](actions/delete-data-route.md) | `DELETE /routes/:id` | [docs](https://www.webmerge.me/developers/routes) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://www.webmerge.me/developers/documents) |
| [Encrypt PDF](actions/encrypt-pdf.md) | `POST /tools/encrypt_pdf` | [docs](https://www.webmerge.me/developers/tools) |
| [Get Data Route](actions/get-data-route.md) | `GET /routes/:id` | [docs](https://www.webmerge.me/developers/routes) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://www.webmerge.me/developers/documents) |
| [Get Document File](actions/get-document-file.md) | `GET /documents/:id/file` | [docs](https://www.webmerge.me/developers/documents) |
| [List Data Route Deliveries](actions/list-data-route-deliveries.md) | `GET /routes/:id/deliveries` | [docs](https://www.webmerge.me/developers/routes) |
| [List Data Route Fields](actions/list-data-route-fields.md) | `GET /routes/:id/fields` | [docs](https://www.webmerge.me/developers/routes) |
| [List Data Route Rules](actions/list-data-route-rules.md) | `GET /routes/:id/rules` | [docs](https://www.webmerge.me/developers/routes) |
| [List Data Routes](actions/list-data-routes.md) | `GET /routes` | [docs](https://www.webmerge.me/developers/routes) |
| [List Document Deliveries](actions/list-document-deliveries.md) | `GET /documents/:id/deliveries` | [docs](https://www.webmerge.me/developers/documents) |
| [List Document Fields](actions/list-document-fields.md) | `GET /documents/:id/fields` | [docs](https://www.webmerge.me/developers/documents) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://www.webmerge.me/developers/documents) |
| [Merge Data Route](actions/merge-data-route.md) | `POST https://www.webmerge.me/route/:id/:key` | [docs](https://www.webmerge.me/developers/routes) |
| [Merge Document](actions/merge-document.md) | `POST https://www.webmerge.me/merge/:id/:key` | [docs](https://www.webmerge.me/developers/documents) |
| [Split PDF](actions/split-pdf.md) | `POST /tools/split_pdf` | [docs](https://www.webmerge.me/developers/tools) |
| [Update Data Route](actions/update-data-route.md) | `PUT /routes/:id` | [docs](https://www.webmerge.me/developers/routes) |
| [Update Document](actions/update-document.md) | `PUT /documents/:id` | [docs](https://www.webmerge.me/developers/documents) |
