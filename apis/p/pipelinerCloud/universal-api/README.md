# <img src="https://images.mindcloud.co/apps/icons/images-11_1774543500188.png" alt="Pipeliner Cloud logo" width="28" height="28"> Pipeliner Cloud: Universal API

Pipeliner Cloud is a CRM platform for managing accounts, contacts, opportunities, leads, activities, products, and related sales data through the Pipeliner Cloud REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipelinerCloud/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pipelinersales.com/
- **Vendor API docs:** https://pipelinercrm.eu.apidog.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Pipeliner Cloud. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing account from Pipeliner Cloud. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Pipeliner Cloud. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Pipeliner Cloud. |
| [Merge Accounts](actions/merge-accounts.md) | PUT | Merges existing accounts in Pipeliner Cloud. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Pipeliner Cloud. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Pipeliner Cloud. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Pipeliner Cloud. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Pipeliner Cloud. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Pipeliner Cloud. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Pipeliner Cloud. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Pipeliner Cloud. |
| [Merge Contacts](actions/merge-contacts.md) | PUT | Merges existing contacts in Pipeliner Cloud. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Pipeliner Cloud. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Pipeliner Cloud. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Pipeliner Cloud. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Pipeliner Cloud. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Pipeliner Cloud. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Pipeliner Cloud. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Pipeliner Cloud. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from Pipeliner Cloud. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from Pipeliner Cloud. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from Pipeliner Cloud. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in Pipeliner Cloud. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Batch Upsert Products](actions/batch-upsert-products.md) | PUT | Creates or updates products in Pipeliner Cloud in batches. |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Pipeliner Cloud. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Pipeliner Cloud. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Pipeliner Cloud. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Pipeliner Cloud. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Pipeliner Cloud. |

