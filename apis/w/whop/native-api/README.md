# Whop: Native API Reference

A consolidated summary of Whop's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.whop.com/developer/api/getting-started
- **API base URL:** `https://api.whop.com`

## Authentication

### Company API Key

Authenticate Whop with a Company API key for company-scoped API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.whop.com/developer/api/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `pageInfo.endCursor`.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get OAuth User Info](actions/get-oauth-user-info.md) | `GET /oauth/userinfo` | [docs](https://docs.whop.com/developer/guides/oauth) |
| [List Companies](actions/list-companies.md) | `GET /api/v1/companies` | [docs](https://docs.whop.com/api-reference/companies/list-companies) |
| [List Experiences](actions/list-experiences.md) | `GET /api/v1/experiences` | [docs](https://docs.whop.com/api-reference/experiences/list-experiences) |
| [List Forum Posts](actions/list-forum-posts.md) | `GET /api/v1/forum_posts` | [docs](https://docs.whop.com/api-reference/forum-posts/list-forum-posts) |
| [List Forums](actions/list-forums.md) | `GET /api/v1/forums` | [docs](https://docs.whop.com/api-reference/forums/list-forums) |
| [List Invoices](actions/list-invoices.md) | `GET /api/v1/invoices` | [docs](https://docs.whop.com/api-reference/invoices/list-invoices) |
| [List Leads](actions/list-leads.md) | `GET /api/v1/leads` | [docs](https://docs.whop.com/api-reference/leads/list-leads) |
| [List Members](actions/list-members.md) | `GET /api/v1/members` | [docs](https://docs.whop.com/api-reference/members/list-members) |
| [List Memberships](actions/list-memberships.md) | `GET /api/v1/memberships` | [docs](https://docs.whop.com/api-reference/memberships/list-memberships) |
| [List Payments](actions/list-payments.md) | `GET /api/v1/payments` | [docs](https://docs.whop.com/api-reference/payments/list-payments) |
| [List Plans](actions/list-plans.md) | `GET /api/v1/plans` | [docs](https://docs.whop.com/api-reference/plans/list-plans) |
| [List Products](actions/list-products.md) | `GET /api/v1/products` | [docs](https://docs.whop.com/api-reference/products/list-products) |
| [List Promo Codes](actions/list-promo-codes.md) | `GET /api/v1/promo_codes` | [docs](https://docs.whop.com/api-reference/promo-codes/list-promo-codes) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /api/v1/companies/:id` | [docs](https://docs.whop.com/api-reference/companies/retrieve-company) |
| [Retrieve Experience](actions/retrieve-experience.md) | `GET /api/v1/experiences/:id` | [docs](https://docs.whop.com/api-reference/experiences/retrieve-experience) |
| [Retrieve Forum](actions/retrieve-forum.md) | `GET /api/v1/forums/:id` | [docs](https://docs.whop.com/api-reference/forums/retrieve-forum) |
| [Retrieve Invoice](actions/retrieve-invoice.md) | `GET /api/v1/invoices/:id` | [docs](https://docs.whop.com/api-reference/invoices/retrieve-invoice) |
| [Retrieve Lead](actions/retrieve-lead.md) | `GET /api/v1/leads/:id` | [docs](https://docs.whop.com/api-reference/leads/retrieve-lead) |
| [Retrieve Member](actions/retrieve-member.md) | `GET /api/v1/members/:id` | [docs](https://docs.whop.com/api-reference/members/retrieve-member) |
| [Retrieve Membership](actions/retrieve-membership.md) | `GET /api/v1/memberships/:id` | [docs](https://docs.whop.com/api-reference/memberships/retrieve-membership) |
| [Retrieve Plan](actions/retrieve-plan.md) | `GET /api/v1/plans/:id` | [docs](https://docs.whop.com/api-reference/plans/retrieve-plan) |
| [Retrieve Product](actions/retrieve-product.md) | `GET /api/v1/products/:id` | [docs](https://docs.whop.com/api-reference/products/retrieve-product) |
| [Retrieve Promo Code](actions/retrieve-promo-code.md) | `GET /api/v1/promo_codes/:id` | [docs](https://docs.whop.com/api-reference/promo-codes/retrieve-promo-code) |
