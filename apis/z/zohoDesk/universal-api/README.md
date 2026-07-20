# <img src="https://images.mindcloud.co/apps/icons/zoho-desk-1024x1024_1775226880891.png" alt="Zoho Desk logo" width="28" height="28"> Zoho Desk: Universal API

Manage Zoho Desk tickets, contacts, accounts, departments, organization metadata, and webhooks from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoDesk/latest
- **Category:** Support / Ticketing
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/desk/
- **Vendor API docs:** https://desk.zoho.com/DeskAPIDocument

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Search Accounts](actions/search-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieve currently installed channels including `System`, `Channel Integration` and `Instant Messaging` channels. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket Comment](actions/create-ticket-comment.md) | POST |  |
| [List Ticket Comments](actions/list-ticket-comments.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Fields In Module](actions/list-organization-fields-in-module.md) | GET |  |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Get Department](actions/get-department.md) | GET |  |
| [List Departments](actions/list-departments.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Layouts](actions/list-layouts.md) | GET | Retrieve a list of all the layouts configured for a module. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [List Threads](actions/list-threads.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET | List Tickets with optional filters |
| [Move Ticket](actions/move-ticket.md) | PUT |  |
| [Search Tickets](actions/search-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieve the configuration details and permissions defined for the profile of the currently logged in user. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

