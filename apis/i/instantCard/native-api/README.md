# InstantCard: Native API Reference

A consolidated summary of InstantCard's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://instantcard.net/api/
- **API base URL:** `https://core.instantcard.net`

## Authentication

### Session Token

Authenticate with InstantCard credentials to obtain a session token.

### Credentials

- **Email:** `email` · required · Email used to sign in to InstantCard.

Send these headers with each API request:

```http
Authorization: Bearer <custom.auth_token>
```

[Official authentication documentation](https://instantcard.net/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cards To Print Job](actions/add-cards-to-print-job.md) | `POST /api/v2/organizations/:organizationId/print_jobs/:id/add_cards` | [docs](https://instantcard.net/api/) |
| [Add Funds](actions/add-funds.md) | `POST /api/v2/organizations/:organizationId/add_funds` | [docs](https://instantcard.net/api/) |
| [Authenticate User](actions/authenticate-user.md) | `POST /api/v2/authenticate?email={{credentials.email}}&password={{credentials.password}}` | [docs](https://instantcard.net/api/) |
| [Check Print Job Balance](actions/check-print-job-balance.md) | `GET /api/v2/organizations/:organizationId/print_jobs/:id/check_balance` | [docs](https://instantcard.net/api/) |
| [Create Address](actions/create-address.md) | `POST /api/v2/organizations/:organizationId/addresses` | [docs](https://instantcard.net/api/) |
| [Create Card](actions/create-card.md) | `POST /api/v2/organizations/:organizationId/cards` | [docs](https://instantcard.net/api/) |
| [Create Contact](actions/create-contact.md) | `POST /api/v2/organizations/:organizationId/contacts` | [docs](https://instantcard.net/api/) |
| [Create Print Job](actions/create-print-job.md) | `POST /api/v2/organizations/:organizationId/print_jobs` | [docs](https://instantcard.net/api/) |
| [Delete Address](actions/delete-address.md) | `DELETE /api/v2/organizations/:organizationId/addresses/:id` | [docs](https://instantcard.net/api/) |
| [Delete Card](actions/delete-card.md) | `DELETE /api/v2/organizations/:organizationId/cards/:id` | [docs](https://instantcard.net/api/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/v2/organizations/:organizationId/contacts/:id` | [docs](https://instantcard.net/api/) |
| [Finalize Card](actions/finalize-card.md) | `PATCH /api/v2/organizations/:organizationId/cards/:id/finalize` | [docs](https://instantcard.net/api/) |
| [Get Address](actions/get-address.md) | `GET /api/v2/organizations/:organizationId/addresses/:id` | [docs](https://instantcard.net/api/) |
| [Get Card](actions/get-card.md) | `GET /api/v2/organizations/:organizationId/cards/:id` | [docs](https://instantcard.net/api/) |
| [Get Card Template Fields](actions/get-card-template-fields.md) | `GET /api/v2/organizations/:organizationId/card_templates/:id/fields` | [docs](https://instantcard.net/api/) |
| [Get Contact](actions/get-contact.md) | `GET /api/v2/organizations/:organizationId/contacts/:id` | [docs](https://instantcard.net/api/) |
| [Get My Profile](actions/get-my-profile.md) | `GET /api/v2/profile/me` | [docs](https://instantcard.net/api/) |
| [Get Organization](actions/get-organization.md) | `GET /api/v2/organizations/:organizationId` | [docs](https://instantcard.net/api/) |
| [Get Organization Balance](actions/get-organization-balance.md) | `GET /api/v2/organizations/:organizationId/balance` | [docs](https://instantcard.net/api/) |
| [Get Print Job](actions/get-print-job.md) | `GET /api/v2/organizations/:organizationId/print_jobs/:id` | [docs](https://instantcard.net/api/) |
| [Get Print Job Charge Details](actions/get-print-job-charge-details.md) | `GET /api/v2/organizations/:organizationId/print_jobs/:id/charge_details` | [docs](https://instantcard.net/api/) |
| [List Addresses](actions/list-addresses.md) | `GET /api/v2/organizations/:organizationId/addresses` | [docs](https://instantcard.net/api/) |
| [List Card Print History](actions/list-card-print-history.md) | `GET /api/v2/organizations/:organizationId/cards/:id/print_history` | [docs](https://instantcard.net/api/) |
| [List Card Templates](actions/list-card-templates.md) | `GET /api/v2/organizations/:organizationId/card_templates` | [docs](https://instantcard.net/api/) |
| [List Cards](actions/list-cards.md) | `GET /api/v2/organizations/:organizationId/cards` | [docs](https://instantcard.net/api/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v2/organizations/:organizationId/contacts` | [docs](https://instantcard.net/api/) |
| [List Financial Transactions](actions/list-financial-transactions.md) | `GET /api/v2/organizations/:organizationId/financial_transactions` | [docs](https://instantcard.net/api/) |
| [List Print Jobs](actions/list-print-jobs.md) | `GET /api/v2/organizations/:organizationId/print_jobs` | [docs](https://instantcard.net/api/) |
| [List Shipping Providers](actions/list-shipping-providers.md) | `GET /api/v2/organizations/:organizationId/shipping_providers` | [docs](https://instantcard.net/api/) |
| [Preview Card](actions/preview-card.md) | `GET /api/v2/organizations/:organizationId/cards/:id/preview` | [docs](https://instantcard.net/api/) |
| [Remove Card From Print Job](actions/remove-card-from-print-job.md) | `DELETE /api/v2/organizations/:organizationId/print_jobs/:id/remove_cards/:cardId` | [docs](https://instantcard.net/api/) |
| [Search Cards](actions/search-cards.md) | `GET /api/v2/organizations/:organizationId/cards/search` | [docs](https://instantcard.net/api/) |
| [Submit Print Job](actions/submit-print-job.md) | `POST /api/v2/organizations/:organizationId/print_jobs/:id/print` | [docs](https://instantcard.net/api/) |
| [Update Address](actions/update-address.md) | `PATCH /api/v2/organizations/:organizationId/addresses/:id` | [docs](https://instantcard.net/api/) |
| [Update Card](actions/update-card.md) | `PATCH /api/v2/organizations/:organizationId/cards/:id` | [docs](https://instantcard.net/api/) |
| [Update Contact](actions/update-contact.md) | `PATCH /api/v2/organizations/:organizationId/contacts/:id` | [docs](https://instantcard.net/api/) |
| [Update Print Job](actions/update-print-job.md) | `PATCH /api/v2/organizations/:organizationId/print_jobs/:id` | [docs](https://instantcard.net/api/) |
