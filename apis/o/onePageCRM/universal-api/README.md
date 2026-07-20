# <img src="https://images.mindcloud.co/apps/icons/one-page-crm_1773153685406.png" alt="OnePageCRM logo" width="28" height="28"> OnePageCRM: Universal API

Track leads, manage contacts, and follow up on sales

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onePageCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.onepagecrm.com/
- **Vendor API docs:** https://developer.onepagecrm.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in OnePageCRM. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from OnePageCRM. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from OnePageCRM. |
| [Mark Action as Done](actions/mark-action-as-done.md) | PUT | Marks an action as done in OnePageCRM. |
| [Update Action](actions/update-action.md) | PUT | Updates an existing action in OnePageCRM. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from OnePageCRM. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from OnePageCRM. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in OnePageCRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Change Contact Owner](actions/change-contact-owner.md) | PUT | Changes a contact's owner in OnePageCRM. |
| [Change Contact Status](actions/change-contact-status.md) | PUT | Changes a contact's status in OnePageCRM. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in OnePageCRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from OnePageCRM. |
| [List Action Stream Contacts](actions/list-action-stream-contacts.md) | GET | Retrieves contacts from OnePageCRM prioritized by next action. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from OnePageCRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in OnePageCRM. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in OnePageCRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from OnePageCRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from OnePageCRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in OnePageCRM. |

### Lead Source

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Sources](actions/list-lead-sources.md) | GET | Retrieves lead sources from OnePageCRM. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in OnePageCRM. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from OnePageCRM. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from OnePageCRM. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from OnePageCRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from OnePageCRM. |

