# <img src="https://images.mindcloud.co/apps/icons/eventgeek-circa-icon-square_1776793294979.png" alt="EventGeek logo" width="28" height="28"> EventGeek: Universal API

Circa API integration for managing events, contacts, companies, teams, event staffing, expenses, exports, and customization fields.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventGeek/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://circa.co
- **Vendor API docs:** https://docs.circa.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in EventGeek. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from EventGeek. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from EventGeek by ID. |
| [List Companies](actions/list-companies.md) | GET | Retrieves company records from your EventGeek account. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in EventGeek. |

### Company Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Company Contacts](actions/list-company-contacts.md) | GET | Retrieves company contact records from EventGeek. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in EventGeek. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from EventGeek. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from EventGeek by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from your EventGeek account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in EventGeek. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in EventGeek. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from EventGeek. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from EventGeek by ID. |
| [List Events](actions/list-events.md) | GET | Retrieves event records from your EventGeek account. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in EventGeek. |

### Event Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Event](actions/add-contact-to-event.md) | POST | Adds a contact to an event in EventGeek. |
| [Get Event Contact](actions/get-event-contact.md) | GET | Retrieves an event contact from EventGeek by ID. |
| [List Event Contacts](actions/list-event-contacts.md) | GET | Retrieves contacts for an event in EventGeek. |
| [Remove Contact From Event](actions/remove-contact-from-event.md) | DELETE | Removes a contact from an event in EventGeek. |
| [Update Event Contact](actions/update-event-contact.md) | PUT | Updates an event contact in EventGeek. |

### Event Contacts Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Event Contacts Export](actions/create-event-contacts-export.md) | POST | Creates an event contacts export in EventGeek. |
| [Delete Event Contacts Export](actions/delete-event-contacts-export.md) | DELETE | Deletes an event contacts export from EventGeek. |
| [Get Event Contacts Export](actions/get-event-contacts-export.md) | GET | Retrieves an event contacts export from EventGeek. |

### Event Expense

| Action | Method | Description |
| --- | --- | --- |
| [List Event Expenses](actions/list-event-expenses.md) | GET | Retrieves event expense records from EventGeek. |

### Event Staff

| Action | Method | Description |
| --- | --- | --- |
| [List Event Staff](actions/list-event-staff.md) | GET | Retrieves event staff records from EventGeek. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Field](actions/get-field.md) | GET | Retrieves a custom field from EventGeek by ID. |
| [List Fields](actions/list-fields.md) | GET | Retrieves custom field records from EventGeek. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from EventGeek by ID. |
| [List Teams](actions/list-teams.md) | GET | Retrieves team records from your EventGeek account. |

