# <img src="https://images.mindcloud.co/apps/icons/favicon-app-dmsales-com-48x48_1777315707981.png" alt="DMSales logo" width="28" height="28"> DMSales: Universal API

DMSales is a sales prospecting and customer engagement platform. This integration exposes DMSales projects, contacts, segments, events, validation, TechScope, and account information through the DMSales REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dMSales/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dmsales.com/en/
- **Vendor API docs:** https://app.dmsales.com/api-doc/default

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact details from DMSales. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from DMSales. |

### Contact Event

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Events](actions/list-contact-events.md) | GET | Retrieves contact events from DMSales. |

### Contact Involvement

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Involvement](actions/get-contact-involvement.md) | GET | Retrieves contact involvement details from DMSales. |

### Contact Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Note](actions/add-contact-note.md) | POST | Creates a contact note in DMSales. |
| [Delete Contact Note](actions/delete-contact-note.md) | DELETE | Deletes an existing contact note from DMSales. |
| [Edit Contact Note](actions/edit-contact-note.md) | PUT | Updates an existing contact note in DMSales. |

### Contact Status

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Statuses](actions/list-contact-statuses.md) | GET | Retrieves contact statuses from DMSales. |

### Contact Tag

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Contact Tags](actions/autocomplete-contact-tags.md) | GET | Finds contact tags in DMSales by partial tag. |

### Custom Event

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Event](actions/add-custom-event.md) | POST | Creates a custom event in DMSales. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in DMSales. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from DMSales. |

### Refer Score Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Refer Score Report ID](actions/get-refer-score-report-id.md) | GET | Retrieves a Refer Score report ID from DMSales. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [List Searches](actions/list-searches.md) | GET | Retrieves searches from DMSales. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a new segment in DMSales. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from DMSales. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from DMSales. |

### Wallet Points

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Points](actions/get-wallet-points.md) | GET | Retrieves wallet points from DMSales. |

