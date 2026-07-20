# gyfti: Native API Reference

A consolidated summary of gyfti's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developer.gyfti.fr/
- **API base URL:** `https://app.gyfti.fr/api/1.1`

## Authentication

### Bearer Token

Use a gyfti access token in the Authorization header as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.gyfti.fr/authentification)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `cursor` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `in`, `lt`, `neq`.

## Sorting

Set the sort field with `sort_field` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact to Email Campaign](actions/add-contact-to-email-campaign.md) | `POST /wf/1_zapier_add_contact_trigger/` | [docs](https://developer.gyfti.fr/automate-your-gifts/add-contact-to-campaign) |
| [Add Contact to Postal Campaign](actions/add-contact-to-postal-campaign.md) | `POST /wf/1_zapier_add_contact_trigger_directe/` | [docs](https://developer.gyfti.fr/automate-your-gifts/add-contact-to-campaign) |
| [Add or Update Store User](actions/add-or-update-store-user.md) | `POST /wf/add-user-store` | [docs](https://developer.gyfti.fr/using-gyfti-store/add-or-update-a-user-in-your-store) |
| [Add Pool to Store User](actions/add-pool-to-store-user.md) | `POST /wf/add-pool` | [docs](https://developer.gyfti.fr/using-gyfti-store/add-a-new-pool-to-your-users) |
| [List Campaigns](actions/list-campaigns.md) | `GET /obj/Campaign` | [docs](https://developer.gyfti.fr/automate-your-gifts/retrieve-your-gyfti-campaigns) |
| [Register New Email Webhook](actions/register-new-email-webhook.md) | `POST /wf/new_hook_email/` | [docs](https://developer.gyfti.fr/retrieve-data-from-campaigns/new-email) |
| [Register New Order Webhook](actions/register-new-order-webhook.md) | `POST /wf/new_hook_order/` | [docs](https://developer.gyfti.fr/retrieve-data-from-campaigns/new-order) |
| [Register Order Update Webhook](actions/register-order-update-webhook.md) | `POST /wf/new_hook_order_update/` | [docs](https://developer.gyfti.fr/retrieve-data-from-campaigns/order-update) |
| [Verify Credentials](actions/verify-credentials.md) | `POST /wf/is_log` | [docs](https://developer.gyfti.fr/authentification) |
