# <img src="https://images.mindcloud.co/apps/icons/octadesk_1775578728287.png" alt="Octadesk logo" width="28" height="28"> Octadesk: Universal API

Octadesk: Centralize conversations, automate support, and manage tickets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/octadesk/latest
- **Category:** Support / Ticketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.octadesk.com
- **Vendor API docs:** https://developers.octadesk.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key](actions/check-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | GET | Checks whether an Octadesk API key is valid. |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get Chat](actions/get-chat.md) | GET | Retrieves a chat from Octadesk by ID. |
| [List Chats](actions/list-chats.md) | GET | Retrieves chats from Octadesk. |

### Chat Event

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Events](actions/list-chat-events.md) | GET | Retrieves events from an Octadesk chat. |

### Chat Message

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Messages](actions/list-chat-messages.md) | GET | Retrieves messages from an Octadesk chat. |
| [Send Chat Message](actions/send-chat-message.md) | POST | Creates a message in an Octadesk chat. |

### Chat Template

| Action | Method | Description |
| --- | --- | --- |
| [List Chat Templates](actions/list-chat-templates.md) | GET | Retrieves chat message templates from Octadesk. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Octadesk. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Octadesk by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Octadesk. |
| [Replace Contact](actions/replace-contact.md) | PUT | Replaces an existing contact in Octadesk. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Octadesk. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Octadesk. |

### Survey Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Submissions](actions/list-survey-submissions.md) | GET | Retrieves survey submissions from Octadesk. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Tags](actions/list-ticket-tags.md) | GET | Retrieves ticket tags from Octadesk. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Octadesk. |

### Ticket Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Channels](actions/list-ticket-channels.md) | GET | Retrieves ticket channels from Octadesk. |

### Ticket Form

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Forms](actions/list-ticket-forms.md) | GET | Retrieves ticket forms from Octadesk. |

### Ticket Group

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Groups](actions/list-ticket-groups.md) | GET | Retrieves ticket groups from Octadesk. |

### Ticket Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Search Ticket Interactions](actions/search-ticket-interactions.md) | GET | Finds ticket interactions in Octadesk. |

### Ticket Priority

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Priorities](actions/list-ticket-priorities.md) | GET | Retrieves ticket priorities from Octadesk. |

### Ticket Status

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Statuses](actions/list-ticket-statuses.md) | GET | Retrieves ticket statuses from Octadesk. |

### Ticket Type

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from Octadesk. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Octadesk by number. |
| [List Ticket Interactions](actions/list-ticket-interactions.md) | GET | Retrieves interactions for an Octadesk ticket. |

### Whatsapp Number

| Action | Method | Description |
| --- | --- | --- |
| [List WhatsApp Numbers](actions/list-whatsapp-numbers.md) | GET | Retrieves WhatsApp numbers from Octadesk. |

