# PrimeGate: Native API Reference

A consolidated summary of PrimeGate's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.primegate.io/support/rabota-s-api-primegate
- **API base URL:** `https://api.primegate.io/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Site ID:** `siteId` · required · PrimeGate project site ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.primegate.io/support/rabota-s-api-primegate)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Contact by City](actions/get-contact-by-city.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Email](actions/get-contact-by-email.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Name](actions/get-contact-by-name.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Out ID](actions/get-contact-by-out-id.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Phone](actions/get-contact-by-phone.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Session ID](actions/get-contact-by-session-id.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Contact by Visitor ID](actions/get-contact-by-visitor-id.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Deal by ID](actions/get-deal-by-id.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [Get Deal by Out ID](actions/get-deal-by-out-id.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Contacts](actions/list-contacts.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Contacts by Ad Campaign](actions/list-contacts-by-ad-campaign.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Contacts by Source](actions/list-contacts-by-source.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Contacts by Traffic Channel](actions/list-contacts-by-traffic-channel.md) | `POST contact/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Deals](actions/list-deals.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Deals by Budget](actions/list-deals-by-budget.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Deals by Lead ID](actions/list-deals-by-lead-id.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Deals by Pipeline ID](actions/list-deals-by-pipeline-id.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Deals by Stage ID](actions/list-deals-by-stage-id.md) | `POST deal/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
| [List Leads](actions/list-leads.md) | `POST lead/get` | [docs](https://www.primegate.io/support/metody-dlya-polucheniya-spiska-sushchnostey) |
