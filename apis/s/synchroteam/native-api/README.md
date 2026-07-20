# Synchroteam: Native API Reference

A consolidated summary of Synchroteam's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.synchroteam.com/v2/
- **API base URL:** `https://ws.synchroteam.com`

## Authentication

### Basic Auth (Domain + Authentication Key)

Synchroteam API uses HTTP Basic auth. Use your Synchroteam domain identifier (the subdomain in https://<domain>.synchroteam.com) as the username and your provider Authentication Key as the password.

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

[Official authentication documentation](https://api.synchroteam.com/v2/#authentication)

## API conventions

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | `PUT /Api/v2/Jobs/Cancel` | [docs](https://api.synchroteam.com/v2/#cancel-job) |
| [Complete Replenishment](actions/complete-replenishment.md) | `PUT /Api/v2/StockRequest/Complete` | [docs](https://api.synchroteam.com/v2/#complete-a-replenishment) |
| [Get Customer](actions/get-customer.md) | `GET /Api/v2/Customer/Details` | [docs](https://api.synchroteam.com/v2/#get-customer) |
| [Get Equipment](actions/get-equipment.md) | `GET /Api/v2/Equipment/Details` | [docs](https://api.synchroteam.com/v2/#get-equipment) |
| [Get Job Detail](actions/get-job-detail.md) | `GET /Api/v2/Jobs/Detail` | [docs](https://api.synchroteam.com/v2/#get-job-detail) |
| [Get Job Photos](actions/get-job-photos.md) | `GET /Api/v2/Jobs/Photos` | [docs](https://api.synchroteam.com/v2/#job-photos) |
| [Get Part Detail](actions/get-part-detail.md) | `GET /Api/v2/Part/Details` | [docs](https://api.synchroteam.com/v2/#get-part-detail) |
| [Get Site](actions/get-site.md) | `GET /Api/v2/Site/Details` | [docs](https://api.synchroteam.com/v2/#get-site) |
| [Get User Detail](actions/get-user-detail.md) | `GET /Api/v2/User/Details` | [docs](https://api.synchroteam.com/v2/#get-user-detail) |
| [Initialize Quantities](actions/initialize-quantities.md) | `PUT /Api/v2/Inventory/Quantities` | [docs](https://api.synchroteam.com/v2/#initialize-the-quantities) |
| [List Customers](actions/list-customers.md) | `GET /Api/v2/Customer/List` | [docs](https://api.synchroteam.com/v2/#list-customers) |
| [List Invoices and Quotations](actions/list-invoices-and-quotations.md) | `POST /Api/v2/Invoices/List` | [docs](https://api.synchroteam.com/v2/#list-invoice-quotation) |
| [List Shared Blocks](actions/list-shared-blocks.md) | `GET /Api/v2/SharedBlocks/List` | [docs](https://api.synchroteam.com/v2/#list-shared-blocks) |
| [List Sites by Customer ID](actions/list-sites-by-customer-id.md) | `GET /Api/v2/Site/List/byCustomer/id/:paramValue` | [docs](https://api.synchroteam.com/v2/#get-sites-list-by-customer-id) |
| [Search Activities](actions/search-activities.md) | `POST /Api/v2/Activities/Search` | [docs](https://api.synchroteam.com/v2/#search-activities) |
| [Search Activity Types](actions/search-activity-types.md) | `POST /Api/v2/ActivityType/Search` | [docs](https://api.synchroteam.com/v2/#search-activity-type) |
| [Search Jobs](actions/search-jobs.md) | `POST /Api/v2/Jobs/Search` | [docs](https://api.synchroteam.com/v2/#search-jobs) |
| [Search Replenishment Requests](actions/search-replenishment-requests.md) | `POST /Api/v2/StockRequest/Search` | [docs](https://api.synchroteam.com/v2/#search-replenishment-requests) |
| [Search Users](actions/search-users.md) | `POST /Api/v2/User/Search` | [docs](https://api.synchroteam.com/v2/#search-user) |
| [Send Activity Type](actions/send-activity-type.md) | `POST /Api/V2/ActivityType/Send` | [docs](https://api.synchroteam.com/v2/#send-activity-type) |
| [Send Attachment](actions/send-attachment.md) | `POST /Api/v2/Attachments/Send` | [docs](https://api.synchroteam.com/v2/#send-attachment) |
| [Send Customer](actions/send-customer.md) | `POST /Api/v2/Customer/Send` | [docs](https://api.synchroteam.com/v2/#send-customer) |
| [Send Equipment](actions/send-equipment.md) | `POST /Api/v2/Equipment/Send` | [docs](https://api.synchroteam.com/v2/#send-equipment) |
| [Send Invoice or Quotation](actions/send-invoice-or-quotation.md) | `POST /Api/v2/Invoices/Send` | [docs](https://api.synchroteam.com/v2/#send-invoice-quotation) |
| [Send Job](actions/send-job.md) | `POST /Api/v2/Jobs/Send` | [docs](https://api.synchroteam.com/v2/#send-job) |
| [Send Part](actions/send-part.md) | `POST /Api/v2/Part/Send` | [docs](https://api.synchroteam.com/v2/#send-part) |
| [Send Site](actions/send-site.md) | `POST /Api/v2/Site/Send` | [docs](https://api.synchroteam.com/v2/#send-site) |
| [Send User](actions/send-user.md) | `POST /Api/v2/User/Send` | [docs](https://api.synchroteam.com/v2/#send-user) |
| [Update Parts Pricing](actions/update-parts-pricing.md) | `PUT /Api/v2/Part/Prices` | [docs](https://api.synchroteam.com/v2/#update-parts-pricing) |
| [Validate Job](actions/validate-job.md) | `PUT /Api/v2/Jobs/Validate` | [docs](https://api.synchroteam.com/v2/#validate-job) |
