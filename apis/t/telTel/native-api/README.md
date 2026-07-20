# TelTel: Native API Reference

A consolidated summary of TelTel's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://doc.teltel.io/en/integration-guide
- **OpenAPI specification:** https://api.teltel.io/v2/api.user.0d9ae995324f03f254d3da8d963d46b2.json
- **API base URL:** `https://api.teltel.io/v2`

## Authentication

### API Key

Use the TelTel account API key. TelTel accepts the key as the `apikey` query parameter or the `X-API-KEY` header; this wrapper uses the shared `apikey` query parameter mapping.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidoc.teltel.io/)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 500; accepted range 1–5000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `lt`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Phone Number To Groups](actions/assign-phone-number-to-groups.md) | `PATCH /dids/my-numbers/{id}/groups` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/my-number-groups.json) |
| [Assign Phone Number To Users](actions/assign-phone-number-to-users.md) | `PATCH /dids/my-numbers/{id}/users` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/my-number-users.json) |
| [Create Call](actions/create-call.md) | `POST /calls` | [docs](https://api.teltel.io/v2/apidoc/paths/calls/calls.json) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contacts.json) |
| [Create Contact Group](actions/create-contact-group.md) | `POST /contacts/groups` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact-groups.json) |
| [Create Contacts](actions/create-contacts.md) | `POST /contacts/bulk` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contacts-bulk.json) |
| [Create SMS Campaign](actions/create-sms-campaign.md) | `POST /sms/campaigns` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaigns.json) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/balance` | [docs](https://api.teltel.io/v2/apidoc/paths/account/balance.json) |
| [Get Autodialer](actions/get-autodialer.md) | `GET /autodialers/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/autodialers/autodialer.json) |
| [Get Available Number Country](actions/get-available-number-country.md) | `GET /dids/new-numbers/countries/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/new-numbers-country.json) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact.json) |
| [Get Contact Group](actions/get-contact-group.md) | `GET /contacts/groups/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact-group.json) |
| [Get Devices](actions/get-devices.md) | `GET /devices` | [docs](https://api.teltel.io/v2/apidoc/paths/devices/devices.json) |
| [Get Inbound SMS Report](actions/get-inbound-sms-report.md) | `GET /sms/inbox/reports/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-inbox/sms-report.json) |
| [Get Phone Number](actions/get-phone-number.md) | `GET /dids/my-numbers/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/my-number.json) |
| [Get SMS Campaign](actions/get-sms-campaign.md) | `GET /sms/campaigns/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaign.json) |
| [Get SMS Report](actions/get-sms-report.md) | `GET /sms/reports/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-outbox/sms-report.json) |
| [Get User Statuses](actions/get-user-statuses.md) | `GET /user-statuses` | [docs](https://api.teltel.io/v2/apidoc/paths/user-statuses/user-statuses.json) |
| [Get Users](actions/get-users.md) | `GET /users` | [docs](https://api.teltel.io/v2/apidoc/paths/users/users.json) |
| [List Autodialers](actions/list-autodialers.md) | `GET /autodialers` | [docs](https://api.teltel.io/v2/apidoc/paths/autodialers/autodialers.json) |
| [List Available Number Countries](actions/list-available-number-countries.md) | `GET /dids/new-numbers/countries` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/new-numbers-countries.json) |
| [List Available Number Price Groups](actions/list-available-number-price-groups.md) | `GET /dids/new-numbers/countries/{id}/price-groups` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/new-numbers-price-groups.json) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://api.teltel.io/v2/apidoc/paths/calls/calls.json) |
| [List Contact Group Contacts](actions/list-contact-group-contacts.md) | `GET /contacts/groups/{id}/contacts` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact-group-contacts.json) |
| [List Contact Groups](actions/list-contact-groups.md) | `GET /contacts/groups` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact-groups.json) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contacts.json) |
| [List Inbound SMS Reports](actions/list-inbound-sms-reports.md) | `GET /sms/inbox/reports` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-inbox/sms-reports.json) |
| [List Number Orders](actions/list-number-orders.md) | `GET /dids/orders` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/orders.json) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /dids/my-numbers` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/my-numbers.json) |
| [List SMS Campaign Actions](actions/list-sms-campaign-actions.md) | `GET /sms/campaigns/{id}/actions` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaign-actions.json) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `GET /sms/campaigns` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaigns.json) |
| [List SMS Reports](actions/list-sms-reports.md) | `GET /sms/reports` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-outbox/sms-reports.json) |
| [Lookup Phone Numbers](actions/lookup-phone-numbers.md) | `GET /numbers/lookup/{numbers}` | [docs](https://api.teltel.io/v2/apidoc/paths/number-lookup.json) |
| [Run SMS Campaign Action](actions/run-sms-campaign-action.md) | `POST /sms/campaigns/{id}/actions` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaign-actions.json) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /sms/bulk/text` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-outbox/sms-text-bulk.json) |
| [Send SMS](actions/send-sms.md) | `POST /sms/text` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-outbox/sms-text.json) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact.json) |
| [Update Contact Group](actions/update-contact-group.md) | `PATCH /contacts/groups/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/contacts/contact-group.json) |
| [Update Phone Number](actions/update-phone-number.md) | `PATCH /dids/my-numbers/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/dids/my-number.json) |
| [Update SMS Campaign](actions/update-sms-campaign.md) | `PATCH /sms/campaigns/{id}` | [docs](https://api.teltel.io/v2/apidoc/paths/sms-campaigns/sms-campaign.json) |
