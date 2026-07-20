# <img src="https://images.mindcloud.co/apps/icons/clip-path-group_1781650135983.png" alt="DataCrush logo" width="28" height="28"> DataCrush: Universal API

DataCrush is a CRM and marketing automation platform with REST API endpoints for contacts, accounts, opportunities, and ecommerce entities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataCrush/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datacrush.la/
- **Vendor API docs:** https://help.datacrush.la/hc/es-419/categories/360004031271-Base-de-Conocimientos

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Contacts](actions/search-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/search-contacts?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Ecommerce Category](actions/create-ecommerce-category.md) | POST | Creates an ecommerce category in DataCrush. |
| [Update Ecommerce Category](actions/update-ecommerce-category.md) | PUT | Updates an ecommerce category in DataCrush. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Search Contacts By Lifecycle](actions/change-contact-email.md) | GET | Finds contacts in DataCrush by lifecycle. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in DataCrush. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from DataCrush. |
| [Search Contacts By Email](actions/import-contacts.md) | GET | Finds contacts in DataCrush by email address. |
| [Search Contacts By Contact Key](actions/ingest-contact-event.md) | GET | Finds contacts in DataCrush by contact key. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in DataCrush by email address. |
| [Search Contacts In List](actions/search-contacts-in-list.md) | GET | Finds contacts in DataCrush by list ID. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in DataCrush. |

### CRM Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Account](actions/add-contact-to-account.md) | PUT | Adds a contact to an account in DataCrush. |
| [Create Account](actions/create-account.md) | POST | Creates a new account in DataCrush. |
| [Delete Account](actions/delete-account.md) | DELETE | Deletes an existing account from DataCrush. |
| [Search Accounts By Domain](actions/import-contacts-to-existing-list.md) | GET | Finds accounts in DataCrush by domain. |
| [Remove Contact From Account](actions/remove-contact-from-account.md) | PUT | Removes a contact from an account in DataCrush. |
| [Search Accounts](actions/search-accounts.md) | GET | Finds accounts in DataCrush by name. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in DataCrush. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Ecommerce Customer](actions/create-ecommerce-customer.md) | POST | Creates an ecommerce customer in DataCrush. |
| [Update Ecommerce Customer](actions/update-ecommerce-customer.md) | PUT | Updates an ecommerce customer in DataCrush. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Opportunity](actions/add-contact-to-opportunity.md) | PUT | Adds a contact to an opportunity in DataCrush. |
| [Change Opportunity Stage](actions/change-opportunity-stage.md) | PUT | Updates an opportunity stage in DataCrush. |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in DataCrush. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from DataCrush. |
| [Remove Contact From Opportunity](actions/remove-contact-from-opportunity.md) | PUT | Removes a contact from an opportunity in DataCrush. |
| [Search Opportunities](actions/search-opportunities.md) | GET | Finds opportunities in DataCrush by name. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in DataCrush. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Ecommerce Order](actions/create-ecommerce-order.md) | POST | Creates an ecommerce order in DataCrush. |
| [Update Ecommerce Order](actions/update-ecommerce-order.md) | PUT | Updates an ecommerce order in DataCrush. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Ecommerce Product](actions/create-ecommerce-product.md) | POST | Creates an ecommerce product in DataCrush. |
| [Update Ecommerce Product](actions/update-ecommerce-product.md) | PUT | Updates an ecommerce product in DataCrush. |

