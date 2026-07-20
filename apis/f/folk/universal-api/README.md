# <img src="https://images.mindcloud.co/apps/icons/folk_1773330190832.png" alt="folk logo" width="28" height="28"> folk: Universal API

Manage contacts, companies, deals, notes, and reminders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/folk/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://folk.app
- **Vendor API docs:** https://developer.folk.app/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in folk. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from folk. |
| [Get Company](actions/get-company.md) | GET | Retrieves a specific company from folk. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of companies from folk. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in folk. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Group Custom Fields](actions/list-group-custom-fields.md) | GET | Retrieves group custom fields for an entity type in folk. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in folk. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from folk. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a specific deal from folk. |
| [List Deals](actions/list-deals.md) | GET | Retrieves a list of deals from folk. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in folk. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from folk. |

### Interactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Interaction](actions/create-interaction.md) | POST | Creates an interaction for a person or company in folk. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in folk. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from folk. |
| [Get Note](actions/get-note.md) | GET | Retrieves a specific note from folk. |
| [List Notes](actions/list-notes.md) | GET | Retrieves a list of notes from folk. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in folk. |

### People

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in folk. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from folk. |
| [Get Person](actions/get-person.md) | GET | Retrieves a specific person from folk. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from folk. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in folk. |

### Reminders

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST | Creates a new reminder in folk. |
| [Delete Reminder](actions/delete-reminder.md) | DELETE | Deletes an existing reminder from folk. |
| [Get Reminder](actions/get-reminder.md) | GET | Retrieves a specific reminder from folk. |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves a list of reminders from folk. |
| [Update Reminder](actions/update-reminder.md) | PUT | Updates an existing reminder in folk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from folk. |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from folk. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from folk. |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in folk. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from folk. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a specific webhook from folk. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from folk. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in folk. |

