# <img src="https://images.mindcloud.co/apps/icons/ellipsend_1774871497001.png" alt="Ellipsend logo" width="28" height="28"> Ellipsend: Universal API

Manage social contacts, labels, statuses, products, and DM workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ellipsend/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ellipsend.com
- **Vendor API docs:** https://api.ellipsend.com/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Statuses](actions/list-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST | Creates a new activity in Ellipsend. |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Ellipsend by ID. |

### Activity Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Type](actions/get-activity-type.md) | GET | Retrieves an activity type from Ellipsend by ID. |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from Ellipsend. |

### Assignee

| Action | Method | Description |
| --- | --- | --- |
| [Get Assignee](actions/get-assignee.md) | GET | Retrieves an assignee from Ellipsend by ID. |
| [List Assignees](actions/list-assignees.md) | GET | Retrieves assignees from Ellipsend. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves your company details from Ellipsend. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Ellipsend by token. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Label](actions/create-label.md) | POST | Creates a new label in Ellipsend. |
| [Delete Label](actions/delete-label.md) | DELETE | Deletes an existing label from Ellipsend. |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Ellipsend by ID. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Ellipsend. |
| [Update Label](actions/update-label.md) | PUT | Updates an existing label in Ellipsend. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Ellipsend. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Ellipsend by ID. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Ellipsend. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Create Status](actions/create-status.md) | POST | Creates a new status in Ellipsend. |
| [Delete Status](actions/delete-status.md) | DELETE | Deletes an existing status from Ellipsend. |
| [Get Status](actions/get-status.md) | GET | Retrieves a status from Ellipsend by ID. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from Ellipsend. |
| [Update Status](actions/update-status.md) | PUT | Updates an existing status in Ellipsend. |

