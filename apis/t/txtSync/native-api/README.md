# TxtSync: Native API Reference

A consolidated summary of TxtSync's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.txtsync.com/
- **API base URL:** `https://api.txtsync.com`

## Authentication

### Client Key + Client Secret + x-api-key

TxtSync requires Basic Authorization built from ClientKey:ClientSecret plus an x-api-key header. This is not an OAuth2 flow.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **API Key (x-api-key):** `apiKey` · required · Required x-api-key header. TxtSync provides a shared starter key for initial testing and can issue a dedicated key later.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.txtsync.com/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `orderby` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Campaign](actions/activate-campaign.md) | `POST /campaigns/:id/activate` | [docs](https://docs.txtsync.com/#activate-campaign) |
| [Add Campaign Connection](actions/add-campaign-connection.md) | `POST /campaigns/:id/connections` | [docs](https://docs.txtsync.com/#add-campaign-connection) |
| [Add Contact Tags](actions/add-contact-tags.md) | `POST /contacts/:id/tags` | [docs](https://docs.txtsync.com/#create-tag-contact-associations) |
| [Check Contact Duplicates](actions/check-contact-duplicates.md) | `GET /contacts/duplicates` | [docs](https://docs.txtsync.com/#contact-duplication-check) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://docs.txtsync.com/#add-campaign) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://docs.txtsync.com/#add-contact) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://docs.txtsync.com/#add-tag) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://docs.txtsync.com/#delete-contact) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://docs.txtsync.com/#delete-tag) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:id` | [docs](https://docs.txtsync.com/#get-campaign) |
| [Get Campaign Report](actions/get-campaign-report.md) | `GET /campaigns/:id/report` | [docs](https://docs.txtsync.com/#campaign-reporting) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://docs.txtsync.com/#get-contact) |
| [Get System Report](actions/get-system-report.md) | `GET /system/report` | [docs](https://docs.txtsync.com/#system-report) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:id` | [docs](https://docs.txtsync.com/#get-tag) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.txtsync.com/#get-campaigns) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /contacts/:id/tags` | [docs](https://docs.txtsync.com/#get-associated-tags) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://docs.txtsync.com/#bulk-get-contacts) |
| [List SMS](actions/list-sms.md) | `GET /sms` | [docs](https://docs.txtsync.com/#bulk-get-sms) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://docs.txtsync.com/#bulk-get-tags) |
| [Preview SMS](actions/preview-sms.md) | `POST /sms/preview` | [docs](https://docs.txtsync.com/#preview-sms) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /sms/bulk` | [docs](https://docs.txtsync.com/#send-bulk-sms) |
| [Send Single SMS](actions/send-single-sms.md) | `POST /sms/send` | [docs](https://docs.txtsync.com/#send-single-sms) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://docs.txtsync.com/#update-contact) |
| [Update Tag](actions/update-tag.md) | `PUT /tags/:id` | [docs](https://docs.txtsync.com/#update-tag) |
