# <img src="https://images.mindcloud.co/apps/icons/whop_1773158235188.png" alt="Whop logo" width="28" height="28"> Whop: Universal API

Whop: Sell digital products, memberships, and community access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whop/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whop.com/
- **Vendor API docs:** https://docs.whop.com/developer/api/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [List Forums](actions/list-forums.md) | GET | Retrieves forums from Whop for a company. |
| [Retrieve Forum](actions/retrieve-forum.md) | GET | Retrieves forum details from the Whop platform. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from the Whop platform. |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves company details from the Whop platform. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Whop for a company. |
| [Retrieve Lead](actions/retrieve-lead.md) | GET | Retrieves lead details from the Whop platform. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Whop for a company. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves invoice details from the Whop platform. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Experiences](actions/list-experiences.md) | GET | Retrieves experiences from Whop for a company. |
| [List Promo Codes](actions/list-promo-codes.md) | GET | Retrieves promo codes from Whop for a company. |
| [Retrieve Experience](actions/retrieve-experience.md) | GET | Retrieves experience details from the Whop platform. |
| [Retrieve Promo Code](actions/retrieve-promo-code.md) | GET | Retrieves promo code details from the Whop platform. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Whop for a company. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Whop for a company. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves product details from the Whop platform. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves members from Whop for a company. |
| [Retrieve Member](actions/retrieve-member.md) | GET | Retrieves member details from the Whop platform. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves subscription plans from Whop for a company. |
| [Retrieve Plan](actions/retrieve-plan.md) | GET | Retrieves plan details from the Whop platform. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Memberships](actions/list-memberships.md) | GET | Retrieves memberships from Whop for a company. |
| [Retrieve Membership](actions/retrieve-membership.md) | GET | Retrieves membership details from the Whop platform. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [List Forum Posts](actions/list-forum-posts.md) | GET | Retrieves forum posts from the Whop platform. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get OAuth User Info](actions/get-oauth-user-info.md) | GET | Retrieves your OAuth user information from Whop. |

