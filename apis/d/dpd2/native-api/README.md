# Dpd2: Native API Reference

A consolidated summary of Dpd2's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://getdpd.com/docs/api/index.html
- **OpenAPI specification:** https://getdpd.com/docs/api/DPDAPIReference.pdf
- **API base URL:** `https://api.getdpd.com/v2`

## Authentication

### DPD Basic Auth

Authenticate with your DPD account username and API password.

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

[Official authentication documentation](https://getdpd.com/docs/api/authentication.html)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://getdpd.com/docs/api/products.html) |
| [Get Storefront](actions/get-storefront.md) | `GET /storefronts/:id` | [docs](https://getdpd.com/docs/api/storefronts.html) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://getdpd.com/docs/api/products.html) |
| [List Storefronts](actions/list-storefronts.md) | `GET /storefronts` | [docs](https://getdpd.com/docs/api/storefronts.html) |
| [Ping](actions/ping.md) | `GET /` | [docs](https://getdpd.com/docs/api/general.html) |
