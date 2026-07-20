# SMSEdge: Native API Reference

A consolidated summary of SMSEdge's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.smsedge.io/reference/getting-started
- **OpenAPI specification:** https://developers.smsedge.io/openapi/59fee63413c2420010230a62
- **API base URL:** `https://api.smsedge.com/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.smsedge.io/reference/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze SMS Text](actions/analyze-sms-text.md) | `POST /text/analyze/` | [docs](https://developers.smsedge.io/reference/text-analyze) |
| [Create Contact](actions/create-contact.md) | `POST /numbers/create/` | [docs](https://developers.smsedge.io/reference/numbers-create) |
| [Create List](actions/create-list.md) | `POST /lists/create/` | [docs](https://developers.smsedge.io/reference/lists-create) |
| [Delete Contacts](actions/delete-contacts.md) | `DELETE /numbers/delete/` | [docs](https://developers.smsedge.io/reference/numbers-delete) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/delete/` | [docs](https://developers.smsedge.io/reference/lists-delete) |
| [Get Automations](actions/get-automations.md) | `GET /automations/getall` | [docs](https://developers.smsedge.io/reference/get-all-automations-1) |
| [Get Campaigns](actions/get-campaigns.md) | `GET /campaigns/getall` | [docs](https://developers.smsedge.io/reference/list-1) |
| [Get Contacts](actions/get-contacts.md) | `GET /numbers/get/` | [docs](https://developers.smsedge.io/reference/numbers-get) |
| [Get Countries](actions/get-countries.md) | `POST /references/countries/` | [docs](https://developers.smsedge.io/reference/references-countries) |
| [Get HTTP Status Codes](actions/get-http-status-codes.md) | `POST /references/statuses/` | [docs](https://developers.smsedge.io/reference/references-statuses) |
| [Get List Details](actions/get-list-details.md) | `GET /lists/info/` | [docs](https://developers.smsedge.io/reference/lists-info) |
| [Get Lists](actions/get-lists.md) | `GET /lists/getall/` | [docs](https://developers.smsedge.io/reference/lists-getall) |
| [Get Routes](actions/get-routes.md) | `GET /routes/getall/` | [docs](https://developers.smsedge.io/reference/routes-getall) |
| [Get Sending Reports](actions/get-sending-reports.md) | `GET /reports/sending/` | [docs](https://developers.smsedge.io/reference/reports-sending) |
| [Get SMS Message Details](actions/get-sms-message-details.md) | `GET /sms/get/` | [docs](https://developers.smsedge.io/reference/sms-get) |
| [Get Unsubscribed Numbers](actions/get-unsubscribed-numbers.md) | `GET /numbers/unsubscribers/` | [docs](https://developers.smsedge.io/reference/numbers-unsubscribers) |
| [Get User Details](actions/get-user-details.md) | `POST /user/details/` | [docs](https://developers.smsedge.io/reference/user-details) |
| [Resubscribe Number](actions/resubscribe-number.md) | `DELETE /numbers/remove-unsubscriber` | [docs](https://developers.smsedge.io/reference/resubscribe-number) |
| [Unsubscribe Number](actions/unsubscribe-number.md) | `POST /numbers/unsubscribe/` | [docs](https://developers.smsedge.io/reference/unsubscribers) |
| [Verify Number Format](actions/verify-number-format.md) | `POST /verify/number-simple/` | [docs](https://developers.smsedge.io/reference/verify-number-simple) |
