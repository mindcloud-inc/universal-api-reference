# Infor ReserveCloud SCS: Native API Reference

A consolidated summary of Infor ReserveCloud SCS's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50066

## Authentication

### Basic

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

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `results`. The current page number is read from `count`.

## Pagination

Use `maxResults` in the query string to set the page size (default 25; accepted range 1–100). Use `firstResult` in the query string as the record offset.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | `GET https://www.reservecloud.com/gateway/request` | [docs](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237) |
| [List Event Services](actions/list-event-services.md) | `GET https://www.reservecloud.com/gateway/request` | [docs](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237) |
| [List Events](actions/list-events.md) | `GET https://www.reservecloud.com/gateway/request` | [docs](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237) |
| [List Functions](actions/list-functions.md) | `GET https://www.reservecloud.com/gateway/request` | [docs](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237) |
| [List Transaction](actions/list-transaction.md) | `GET https://www.reservecloud.com/gateway/request` | [docs](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.reservecloud.com/web/university/universityDocumentDownloadViewable/50237) |
