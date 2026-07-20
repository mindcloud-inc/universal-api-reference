# ClickSend SMS: Native API Reference

A consolidated summary of ClickSend SMS's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.clicksend.com/docs
- **OpenAPI specification:** https://developers.clicksend.com/docs/_spec/messaging/sms.json?download=
- **API base URL:** `https://rest.clicksend.com`

## Authentication

### Basic Auth

Use ClickSend API Username as username and API Key as password.

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

[Official authentication documentation](https://developers.clicksend.com/docs/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `data.last_page`. The current page number is read from `data.current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 15; accepted range 15–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate SMS Campaign Price](actions/calculate-sms-campaign-price.md) | `POST /v3/sms-campaigns/price` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/calculate-sms-campaign-price/) |
| [Calculate SMS Price](actions/calculate-sms-price.md) | `POST /v3/sms/price` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/calculate-sms-price) |
| [Cancel SMS](actions/cancel-sms.md) | `PUT /v3/sms/:message_id/cancel` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/cancel-sms) |
| [Cancel SMS Campaign](actions/cancel-sms-campaign.md) | `PUT /v3/sms-campaigns/:sms_campaign_id/cancel` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/other/view-sms-campaigns) |
| [Create Contact](actions/create-contact.md) | `POST /v3/lists/:list_id/contacts` | [docs](https://developers.clicksend.com/docs/contacts/lists/other/create-list) |
| [Create List](actions/create-list.md) | `POST /v3/lists` | [docs](https://developers.clicksend.com/docs/contacts/lists/other/create-list) |
| [Create SMS Template](actions/create-sms-template.md) | `POST /v3/sms/templates` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/create-sms-template/) |
| [Delete SMS Template](actions/delete-sms-template.md) | `DELETE /v3/sms/templates/:template_id` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/delete-sms-template/) |
| [Export SMS History](actions/export-sms-history.md) | `GET /v3/sms/history/export` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/export-sms-history/) |
| [Get Inbound SMS](actions/get-inbound-sms.md) | `GET /v3/sms/inbound/:original_message_id` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-a-specific-inbound-sms-message) |
| [Get SMS Campaign](actions/get-sms-campaign.md) | `GET /v3/sms-campaigns/:sms_campaign_id` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/view-a-specific-sms-campaign/) |
| [Get SMS Receipt](actions/get-sms-receipt.md) | `GET /v3/sms/receipts/:message_id` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-specific-sms-receipt) |
| [Get SMS Template](actions/get-sms-template.md) | `GET /v3/sms/templates/:template_id` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-a-specific-sms-template/) |
| [Import Contacts](actions/import-contacts.md) | `POST /v3/lists/:list_id/import` | [docs](https://developers.clicksend.com/docs/contacts/lists/other/create-list) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /v3/lists` | [docs](https://developers.clicksend.com/docs/contacts/lists/other/create-list) |
| [List Contacts](actions/list-contacts.md) | `GET /v3/lists/:list_id/contacts` | [docs](https://developers.clicksend.com/docs/contacts/lists/other/create-list) |
| [List Inbound SMS](actions/list-inbound-sms.md) | `GET /v3/sms/inbound` | [docs](https://developers.clicksend.com/docs/messaging/sms/inbound-sms/) |
| [List Numbers](actions/list-numbers.md) | `GET /v3/numbers` | [docs](https://developers.clicksend.com/docs/messaging/sender_ids/numbers/other/purchase-dedicated-number) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `GET /v3/sms-campaigns` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/view-sms-campaigns/) |
| [List SMS History](actions/list-sms-history.md) | `GET /v3/sms/history` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-history) |
| [List SMS Receipts](actions/list-sms-receipts.md) | `GET /v3/sms/receipts` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-receipts) |
| [List SMS Templates](actions/list-sms-templates.md) | `GET /v3/sms/templates` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/view-sms-templates/) |
| [Mark Inbound SMS as Read](actions/mark-inbound-sms-as-read.md) | `PUT /v3/sms/inbound-read` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/mark-inbound-sms-as-read) |
| [Mark SMS Receipt As Read](actions/mark-sms-receipt-as-read.md) | `PUT /v3/sms/receipts-read` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/mark-sms-receipt-as-read) |
| [Request Alpha Tag](actions/request-alpha-tag.md) | `POST /v3/alpha-tags` | [docs](https://developers.clicksend.com/docs/messaging/sender_ids/alpha-tags) |
| [Send SMS](actions/send-sms.md) | `POST /v3/sms/send` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/send-sms) |
| [Send SMS Campaign](actions/send-sms-campaign.md) | `POST /v3/sms-campaigns/send` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/send-sms-campaign/) |
| [Update SMS Campaign](actions/update-sms-campaign.md) | `PUT /v3/sms-campaigns/:sms_campaign_id` | [docs](https://developers.clicksend.com/docs/messaging/sms-campaigns/other/view-sms-campaigns) |
| [Update SMS Template](actions/update-sms-template.md) | `PUT /v3/sms/templates/:template_id` | [docs](https://developers.clicksend.com/docs/messaging/sms/other/update-sms-template/) |
