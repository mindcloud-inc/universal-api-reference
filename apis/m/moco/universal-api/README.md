# <img src="https://images.mindcloud.co/apps/icons/moco_1773261432020.png" alt="Moco logo" width="28" height="28"> Moco: Universal API

Track project time, manage invoices, and view team workloads in MOCO

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moco/latest
- **Category:** Productivity / Project Management
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mocoapp.com/
- **Vendor API docs:** https://everii-group.github.io/mocoapp-api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | POST |  |
| [Update Activity](actions/update-activity.md) | PUT |  |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET |  |
| [List Activities](actions/list-activities.md) | GET |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Comment](actions/get-comment.md) | GET |  |
| [List Comments](actions/list-comments.md) | GET |  |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Update Comment](actions/update-comment.md) | PUT |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal](actions/get-deal.md) | GET |  |
| [List Deals](actions/list-deals.md) | GET |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST |  |
| [Update Deal](actions/update-deal.md) | PUT |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase](actions/create-purchase.md) | POST |  |
| [Update Purchase](actions/update-purchase.md) | PUT |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Update Invoice Status](actions/update-invoice-status.md) | PUT |  |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Offer](actions/get-offer.md) | GET |  |
| [List Offers](actions/list-offers.md) | GET |  |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer](actions/create-offer.md) | POST |  |
| [Update Offer Status](actions/update-offer-status.md) | PUT |  |

### Planning Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Planning Entries](actions/list-planning-entries.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Assigned Projects](actions/list-assigned-projects.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase](actions/get-purchase.md) | GET |  |
| [List Purchases](actions/list-purchases.md) | GET |  |

### Resource Allocations

| Action | Method | Description |
| --- | --- | --- |
| [Create Planning Entry](actions/create-planning-entry.md) | POST |  |
| [Update Planning Entry](actions/update-planning-entry.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Schedules](actions/list-schedules.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Update Schedule](actions/update-schedule.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Update User](actions/update-user.md) | PUT |  |

