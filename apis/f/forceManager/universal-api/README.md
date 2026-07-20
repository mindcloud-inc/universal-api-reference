# <img src="https://images.mindcloud.co/apps/icons/force-manager_1776290877712.png" alt="ForceManager logo" width="28" height="28"> ForceManager: Universal API

ForceManager (Sage Sales Management) REST API integration for CRM records such as companies, contacts, activities, opportunities, products, users, calendars, views, sales orders, and list-of-values resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/forceManager/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.forcemanager.com/
- **Vendor API docs:** https://support.forcemanager.net/en/articles/8613479-using-restful-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read Activities](actions/read-activities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in ForceManager. |
| [Delete Activity](actions/delete-activity.md) | DELETE | Deletes an existing activity from ForceManager. |
| [Read Activities](actions/read-activities.md) | GET | Retrieves activities from your ForceManager account. |
| [Update Activity](actions/update-activity.md) | PUT | Updates an existing activity in ForceManager. |

### Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar](actions/create-calendar.md) | POST | Creates a new calendar in ForceManager. |
| [Delete Calendar](actions/delete-calendar.md) | DELETE | Deletes an existing calendar from ForceManager. |
| [Read Calendars](actions/read-calendars.md) | GET | Retrieves calendars from your ForceManager account. |
| [Update Calendar](actions/update-calendar.md) | PUT | Updates an existing calendar in ForceManager. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in ForceManager. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from ForceManager. |
| [Read Companies](actions/read-companies.md) | GET | Retrieves companies from your ForceManager account. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in ForceManager. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ForceManager. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from ForceManager. |
| [Read Contacts](actions/read-contacts.md) | GET | Retrieves contacts from your ForceManager account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ForceManager. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in ForceManager. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from ForceManager. |
| [Read Opportunities](actions/read-opportunities.md) | GET | Retrieves opportunities from your ForceManager account. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in ForceManager. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in ForceManager. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from ForceManager. |
| [Read Products](actions/read-products.md) | GET | Retrieves products from your ForceManager account. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in ForceManager. |

### Sales Order

| Action | Method | Description |
| --- | --- | --- |
| [Read Sales Orders](actions/read-sales-orders.md) | GET | Retrieves sales orders from your ForceManager account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Read Users](actions/read-users.md) | GET | Retrieves users from your ForceManager account. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a new view in ForceManager. |
| [Delete View](actions/delete-view.md) | DELETE | Deletes an existing view from ForceManager. |
| [Read Views](actions/read-views.md) | GET | Retrieves views from your ForceManager account. |
| [Update View](actions/update-view.md) | PUT | Updates an existing view in ForceManager. |

