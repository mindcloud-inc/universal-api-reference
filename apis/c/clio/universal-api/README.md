# <img src="https://images.mindcloud.co/apps/icons/clio-icon_1773183115534.png" alt="Clio Manage logo" width="28" height="28"> Clio Manage: Universal API

Manage contacts, matters, tasks, notes, and calendar entries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clio.com/manage/
- **Vendor API docs:** https://docs.developers.clio.com/api-docs/clio-manage/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Clio Manage by activity ID. |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from your Clio Manage account. |

### Activity Description

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Description](actions/get-activity-description.md) | GET | Retrieves an activity description from Clio Manage by ID. |
| [List Activity Descriptions](actions/list-activity-descriptions.md) | GET | Retrieves activity descriptions from Clio Manage. |

### Activity Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Rate](actions/get-activity-rate.md) | GET | Retrieves an activity rate from Clio Manage by ID. |
| [List Activity Rates](actions/list-activity-rates.md) | GET | Retrieves activity rates from Clio Manage. |

### Allocation

| Action | Method | Description |
| --- | --- | --- |
| [List Allocations](actions/list-allocations.md) | GET | Retrieves allocations from your Clio Manage account. |

### Calendar Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar Entry](actions/get-calendar-entry.md) | GET | Retrieves a calendar entry from Clio Manage by entry ID. |
| [List Calendar Entries](actions/list-calendar-entries.md) | GET | Retrieves calendar entries from Clio Manage. |

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Calendar Entry](actions/create-calendar-entry.md) | POST | Creates a new calendar entry in Clio Manage. |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [Get Calendar](actions/get-calendar.md) | GET | Retrieves a calendar from Clio Manage by calendar ID. |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves calendars from your Clio Manage account. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Clio Manage by contact ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Clio Manage account. |

### Email Address

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Email Addresses](actions/list-contact-email-addresses.md) | GET | Retrieves email addresses for a contact in Clio Manage. |

### Matter

| Action | Method | Description |
| --- | --- | --- |
| [Create Matter](actions/create-matter.md) | POST | Creates a new matter in Clio Manage. |
| [Get Matter](actions/get-matter.md) | GET | Retrieves a matter from Clio Manage by matter ID. |
| [List Matters](actions/list-matters.md) | GET | Retrieves matters from your Clio Manage account. |
| [Update Matter](actions/update-matter.md) | PUT | Updates a matter in Clio Manage by matter ID. |

### Matter Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Matter Contacts](actions/list-matter-contacts.md) | GET | Retrieves contacts for a matter in Clio Manage. |

### Matter Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Matter Note](actions/create-matter-note.md) | POST | Creates a new matter note in Clio Manage. |

### Matter Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Matter Stages](actions/list-matter-stages.md) | GET | Retrieves matter stages from Clio Manage. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from Clio Manage by note ID. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from your Clio Manage account. |

### Person Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Contact](actions/create-person-contact.md) | POST | Creates a new person contact in Clio Manage. |
| [Update Person Contact](actions/update-person-contact.md) | PUT | Updates a person contact in Clio Manage by contact ID. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Phone Numbers](actions/list-contact-phone-numbers.md) | GET | Retrieves phone numbers for a contact in Clio Manage. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Clio Manage. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Clio Manage by task ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Clio Manage account. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Clio Manage by task ID. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Clio Manage. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity Description](actions/create-activity-description.md) | POST | Creates a new activity description in Clio Manage. |
| [Create Activity Rate](actions/create-activity-rate.md) | POST | Creates a new activity rate in Clio Manage. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Clio Manage. |

