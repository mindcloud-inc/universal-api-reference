# <img src="https://images.mindcloud.co/apps/icons/r-aynetcrm_1774631817697.png" alt="RAYNET CRM logo" width="28" height="28"> RAYNET CRM: Universal API

RAYNET CRM is a cloud CRM for managing accounts, contacts, leads, deals, products, projects, activities, documents, and related sales workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rAYNETCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://raynetcrm.com/
- **Vendor API docs:** https://app.raynetcrm.com/api/doc/index-en.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Delete Company](actions/delete-company.md) | DELETE |  |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST |  |
| [Delete Deal](actions/delete-deal.md) | DELETE |  |
| [Get Deal](actions/get-deal.md) | GET |  |
| [List Deals](actions/list-deals.md) | GET |  |
| [Update Deal](actions/update-deal.md) | PUT |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Convert Lead](actions/convert-lead.md) | PUT |  |
| [Create Lead](actions/create-lead.md) | POST |  |
| [Delete Lead](actions/delete-lead.md) | DELETE |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Lead](actions/update-lead.md) | PUT |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

