# <img src="https://images.mindcloud.co/apps/icons/lead-dyno_1778097698529.png" alt="LeadDyno logo" width="28" height="28"> LeadDyno: Universal API

Manage affiliates, leads, commissions, purchases, and campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadDyno/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leaddyno.com
- **Vendor API docs:** https://app.theneo.io/leaddyno/leaddyno-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Total Lead Count](actions/retrieve-total-lead-count.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-total-lead-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Affiliate

| Action | Method | Description |
| --- | --- | --- |
| [Approve Affiliate](actions/approve-affiliate.md) | PUT | Approves an affiliate account in LeadDyno. |
| [Archive Affiliate](actions/archive-affiliate.md) | PUT | Archives an affiliate account in LeadDyno. |
| [Create Affiliate](actions/create-affiliate.md) | POST | Creates a new affiliate in LeadDyno. |
| [List Affiliates](actions/list-affiliates.md) | GET | Retrieves affiliates from your LeadDyno account. |
| [Reject Affiliate](actions/reject-affiliate.md) | PUT | Rejects an affiliate account in LeadDyno. |
| [Retrieve Affiliate By Code](actions/retrieve-affiliate-by-code.md) | GET | Retrieves an affiliate from LeadDyno by affiliate code. |
| [Retrieve Affiliate By Email](actions/retrieve-affiliate-by-email.md) | GET | Retrieves an affiliate from LeadDyno by email. |
| [Retrieve Affiliate By ID](actions/retrieve-affiliate-by-id.md) | GET | Retrieves an affiliate from LeadDyno by ID. |
| [Unarchive Affiliate](actions/unarchive-affiliate.md) | PUT | Unarchives an affiliate account in LeadDyno. |
| [Update Affiliate](actions/update-affiliate.md) | PUT | Updates an existing affiliate in LeadDyno. |

### Affiliate Commission

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Affiliate Commissions](actions/retrieve-affiliate-commissions.md) | GET | Retrieves commissions for a specific affiliate in LeadDyno. |

### Affiliate Commission Total

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Affiliate Commission Total](actions/retrieve-affiliate-commission-total.md) | GET | Retrieves commission totals for a specific affiliate in LeadDyno. |

### Affiliate Lead

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Affiliate Leads](actions/retrieve-affiliate-leads.md) | GET | Retrieves leads for a specific affiliate in LeadDyno. |

### Affiliate Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Affiliate Purchases](actions/retrieve-affiliate-purchases.md) | GET | Retrieves purchases for a specific affiliate in LeadDyno. |

### Affiliate Sign-in Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Affiliate Sign-In Link](actions/generate-affiliate-sign-in-link.md) | GET | Generates a time-limited sign-in link for an affiliate in LeadDyno. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your LeadDyno account. |
| [Retrieve Campaign By ID](actions/retrieve-campaign-by-id.md) | GET | Retrieves a campaign from LeadDyno by ID. |

### Commission

| Action | Method | Description |
| --- | --- | --- |
| [Create Affiliate Commission](actions/create-affiliate-commission.md) | POST | Creates a new commission for an affiliate in LeadDyno. |
| [List Commissions](actions/list-commissions.md) | GET | Retrieves commissions from your LeadDyno account. |
| [Mark Commissions As Paid](actions/mark-commissions-as-paid.md) | PUT | Marks affiliate commissions as paid for a purchase in LeadDyno. |

### Commission Totals

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Commission Totals](actions/retrieve-commission-totals.md) | GET | Retrieves commission totals from your LeadDyno account. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in LeadDyno. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from your LeadDyno account. |
| [Retrieve Lead By Email](actions/retrieve-lead-by-email.md) | GET | Retrieves a lead from LeadDyno by email. |
| [Retrieve Lead By ID](actions/retrieve-lead-by-id.md) | GET | Retrieves a lead from LeadDyno by ID. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in LeadDyno. |

### Lead Count

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Total Lead Count](actions/retrieve-total-lead-count.md) | GET | Retrieves the total number of leads in LeadDyno. |

### Lead Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Lead Purchases](actions/retrieve-lead-purchases.md) | GET | Retrieves purchases for a specific lead in LeadDyno. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Approve Purchase](actions/approve-purchase.md) | PUT | Approves a pending purchase in LeadDyno. |
| [Create Purchase](actions/create-purchase.md) | POST | Creates a new purchase in LeadDyno. |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves purchases from your LeadDyno account. |
| [Reject Purchase](actions/reject-purchase.md) | PUT | Rejects a pending purchase in LeadDyno. |
| [Retrieve Purchase By Code](actions/retrieve-purchase-by-code.md) | GET | Retrieves a purchase from LeadDyno by purchase code. |
| [Retrieve Purchase By ID](actions/retrieve-purchase-by-id.md) | GET | Retrieves a purchase from LeadDyno by ID. |
| [Update Purchase](actions/update-purchase.md) | PUT | Updates an existing purchase in LeadDyno. |

### Purchase Commission

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Purchase Commissions](actions/retrieve-purchase-commissions.md) | GET | Retrieves commissions for a specific purchase in LeadDyno. |

### Purchase Count

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Total Purchase Count](actions/retrieve-total-purchase-count.md) | GET | Retrieves the total number of purchases in LeadDyno. |

### Visitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Visitor](actions/create-visitor.md) | POST | Creates a new visitor in LeadDyno. |
| [List Visitors](actions/list-visitors.md) | GET | Retrieves visitors from your LeadDyno account. |

### Visitor Count

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Total Visitor Count](actions/retrieve-total-visitor-count.md) | GET | Retrieves the total number of visitors in LeadDyno. |

