# Tolq: Native API Reference

A consolidated summary of Tolq's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.tolq.com/reference
- **API base URL:** `https://api.tolq.com/v1`

## Authentication

### Access Key + Secret

Tolq authenticates with HTTP Basic auth using your Tolq access key as the username and your API secret as the password.

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

[Official authentication documentation](https://docs.tolq.com/reference/access-keys)

## Pagination

Use `per_page` in the query string to set the page size (default 25; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Quote Request](actions/create-quote-request.md) | `POST /translations/requests/quote` | [docs](https://docs.tolq.com/reference/create-a-quote) |
| [Create Translation Request](actions/create-translation-request.md) | `POST /translations/requests` | [docs](https://docs.tolq.com/reference/post-a-translation-request) |
| [Get Translation Request](actions/get-translation-request.md) | `GET /translations/requests/:id` | [docs](https://docs.tolq.com/reference/get-a-translation-request) |
| [Get Uploaded File Info](actions/get-uploaded-file-info.md) | `GET /translations/requests/files/:uid` | [docs](https://docs.tolq.com/reference/uploaded-file-info) |
| [Initiate File Upload](actions/initiate-file-upload.md) | `POST /translations/requests/upload` | [docs](https://docs.tolq.com/reference/initiate-a-file-upload) |
| [List Translation Requests](actions/list-translation-requests.md) | `GET /translations/requests` | [docs](https://docs.tolq.com/reference/list-all-requests) |
| [Order a Quoted Request](actions/order-a-quoted-request.md) | `POST /translations/requests/:id/order` | [docs](https://docs.tolq.com/reference/order-a-quoted-request) |
| [Order an Uploaded File](actions/order-an-uploaded-file.md) | `POST /translations/requests/files/:uid` | [docs](https://docs.tolq.com/reference/order-an-uploaded-file) |
| [Quote an Uploaded File](actions/quote-an-uploaded-file.md) | `POST /translations/requests/files/quote/:uid` | [docs](https://docs.tolq.com/reference/quote-an-uploaded-file) |
