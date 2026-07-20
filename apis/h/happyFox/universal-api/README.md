# <img src="https://images.mindcloud.co/apps/icons/images-1_1773330398344.png" alt="HappyFox logo" width="28" height="28"> HappyFox: Universal API

HappyFox: Manage support tickets, contacts, contact groups, and help desk metadata across tenant-specific HappyFox domains.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/happyFox/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.happyfox.com/
- **Vendor API docs:** https://support.happyfox.com/kb/article/360-api-for-happyfox/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tickets](actions/list-tickets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from HappyFox. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in HappyFox. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from HappyFox. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from HappyFox. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in HappyFox. |

### Contact Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET | Retrieves contact custom fields from HappyFox. |

### Contact Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Group](actions/create-contact-group.md) | POST | Creates a new contact group in HappyFox. |
| [List Contact Groups](actions/list-contact-groups.md) | GET | Retrieves contact groups from HappyFox. |
| [Remove Contacts from Contact Group](actions/remove-contacts-from-contact-group.md) | PUT | Removes contacts from a HappyFox contact group. |
| [Update Contact Group](actions/update-contact-group.md) | PUT | Updates an existing contact group in HappyFox. |
| [Update Contact Group Members](actions/update-contact-group-members.md) | PUT | Updates contacts in a HappyFox contact group. |

### Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Priorities](actions/list-priorities.md) | GET | Retrieves priorities from HappyFox. |

### Staff

| Action | Method | Description |
| --- | --- | --- |
| [List Staff](actions/list-staff.md) | GET | Retrieves staff members from HappyFox. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from HappyFox. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Add Staff Private Note](actions/add-staff-private-note.md) | POST | Adds a private note to a ticket in HappyFox. |
| [Add Staff Update](actions/add-staff-update.md) | POST | Adds a staff update to a ticket in HappyFox. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in HappyFox. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from HappyFox. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from HappyFox. |
| [Move Ticket](actions/move-ticket.md) | PUT | Moves a ticket to another category in HappyFox. |
| [Update Ticket Custom Fields](actions/update-ticket-custom-fields.md) | PUT | Updates a ticket's custom fields in HappyFox. |
| [Update Ticket Properties](actions/update-ticket-properties.md) | PUT | Updates ticket properties in HappyFox. |
| [Update Ticket Tags](actions/update-ticket-tags.md) | PUT | Updates a ticket's tags in HappyFox. |

### Ticket Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Custom Fields](actions/list-ticket-custom-fields.md) | GET | Retrieves ticket custom fields from HappyFox. |

