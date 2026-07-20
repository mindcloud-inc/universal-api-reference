# LeadDyno: Native API Reference

A consolidated summary of LeadDyno's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://app.theneo.io/leaddyno/leaddyno-rest-api
- **API base URL:** `https://api.leaddyno.com/v1`

## Authentication

### API Key

Authenticate requests with a LeadDyno private API key.

### Credentials

- **Private API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.leaddyno.com/hc/en-us/articles/15151748798877-REST-API-Introduction)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Affiliate](actions/approve-affiliate.md) | `POST /affiliates/:id/approve` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates-id-approve) |
| [Approve Purchase](actions/approve-purchase.md) | `POST /purchases/:id/approve` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/approve-a-purchase-by-id) |
| [Archive Affiliate](actions/archive-affiliate.md) | `POST /affiliates/:id/archive` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates-id-archive) |
| [Create Affiliate](actions/create-affiliate.md) | `POST /affiliates` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates) |
| [Create Affiliate Commission](actions/create-affiliate-commission.md) | `POST /affiliates/:id/commissions` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/post-affiliates-id-commissions) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/create-a-lead) |
| [Create Purchase](actions/create-purchase.md) | `POST /purchases` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/post-purchases) |
| [Create Visitor](actions/create-visitor.md) | `POST /visitors` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/visitors/create-a-visitor) |
| [Generate Affiliate Sign-In Link](actions/generate-affiliate-sign-in-link.md) | `POST /affiliates/:id/sign_in_link` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/create-a-new-affiliate-copy) |
| [List Affiliates](actions/list-affiliates.md) | `GET /affiliates` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/campaigns/get-campaigns) |
| [List Commissions](actions/list-commissions.md) | `GET /commissions` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/get-commissions) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/list-all-leads) |
| [List Purchases](actions/list-purchases.md) | `GET /purchases` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases) |
| [List Visitors](actions/list-visitors.md) | `GET /visitors` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/visitors/list-all-visitors) |
| [Mark Commissions As Paid](actions/mark-commissions-as-paid.md) | `POST /commissions/mark_as_paid` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/mark-affiliate-commissions-as-paid) |
| [Reject Affiliate](actions/reject-affiliate.md) | `POST /affiliates/:id/reject` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates-id-reject) |
| [Reject Purchase](actions/reject-purchase.md) | `POST /purchases/:id/reject` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/reject-a-purchase-by-id) |
| [Retrieve Affiliate By Code](actions/retrieve-affiliate-by-code.md) | `GET /affiliates/by_affiliate_code` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates-by-affiliate-code) |
| [Retrieve Affiliate By Email](actions/retrieve-affiliate-by-email.md) | `GET /affiliates/by_email` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates-by-email) |
| [Retrieve Affiliate By ID](actions/retrieve-affiliate-by-id.md) | `GET /affiliates/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates-id) |
| [Retrieve Affiliate Commission Total](actions/retrieve-affiliate-commission-total.md) | `GET /affiliates/:id/commissions_total` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/retrieve-total-commissions-for-a-specific-affiliate) |
| [Retrieve Affiliate Commissions](actions/retrieve-affiliate-commissions.md) | `GET /affiliates/:id/commissions` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/get-affiliates-id-commissions) |
| [Retrieve Affiliate Leads](actions/retrieve-affiliate-leads.md) | `GET /affiliates/:id/leads` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates-id-leads) |
| [Retrieve Affiliate Purchases](actions/retrieve-affiliate-purchases.md) | `GET /affiliates/:id/purchases` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/get-affiliates-id-purchases) |
| [Retrieve Campaign By ID](actions/retrieve-campaign-by-id.md) | `GET /campaigns/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/campaigns/get-campaigns-id) |
| [Retrieve Commission Totals](actions/retrieve-commission-totals.md) | `GET /commissions/totals` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/commissions/get-commissions-totals) |
| [Retrieve Lead By Email](actions/retrieve-lead-by-email.md) | `GET /leads/by_email` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/retrieve-a-lead-by-email) |
| [Retrieve Lead By ID](actions/retrieve-lead-by-id.md) | `GET /leads/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/retrieve-a-lead-by-id) |
| [Retrieve Lead Purchases](actions/retrieve-lead-purchases.md) | `GET /leads/:id/purchases` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/retrieve-purchases-for-a-lead) |
| [Retrieve Purchase By Code](actions/retrieve-purchase-by-code.md) | `GET /purchases/by_purchase_code` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-by-purchase-code) |
| [Retrieve Purchase By ID](actions/retrieve-purchase-by-id.md) | `GET /purchases/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-id) |
| [Retrieve Purchase Commissions](actions/retrieve-purchase-commissions.md) | `GET /purchases/:id/commissions` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-id-commissions) |
| [Retrieve Total Lead Count](actions/retrieve-total-lead-count.md) | `GET /leads/count` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/get-leads-count) |
| [Retrieve Total Purchase Count](actions/retrieve-total-purchase-count.md) | `GET /purchases/count` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/get-purchases-count) |
| [Retrieve Total Visitor Count](actions/retrieve-total-visitor-count.md) | `GET /visitors/count` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/visitors/retrieve-total-visitor-count) |
| [Unarchive Affiliate](actions/unarchive-affiliate.md) | `POST /affiliates/:id/unarchive` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/post-affiliates-id-unarchive) |
| [Update Affiliate](actions/update-affiliate.md) | `PUT /affiliates/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/put-affiliates-id) |
| [Update Lead](actions/update-lead.md) | `PUT /leads/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/update-a-lead) |
| [Update Purchase](actions/update-purchase.md) | `PUT /purchases/:id` | [docs](https://app.theneo.io/leaddyno/leaddyno-rest-api/purchases/update-a-purchase) |
