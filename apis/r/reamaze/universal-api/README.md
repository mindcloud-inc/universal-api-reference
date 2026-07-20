# <img src="https://images.mindcloud.co/apps/icons/reamaze-icon_1773948900798.png" alt="Reamaze logo" width="28" height="28"> Reamaze: Universal API

Reamaze is a customer support platform for conversations, contacts, channels, knowledge base content, staff workflows, response templates, reports, and status-page incidents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reamaze/latest
- **Category:** Support / Ticketing
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reamaze.com
- **Vendor API docs:** https://www.reamaze.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Conversations](actions/list-conversations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST |  |
| [Get Article](actions/get-article.md) | GET |  |
| [List Articles](actions/list-articles.md) | GET |  |
| [Update Article](actions/update-article.md) | PUT |  |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET |  |
| [List Channels](actions/list-channels.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Identity

| Action | Method | Description |
| --- | --- | --- |
| [Create Identity](actions/create-identity.md) | POST |  |
| [List Contact Identities](actions/list-contact-identities.md) | GET |  |

### Contact Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST |  |
| [Delete Contact Note](actions/delete-contact-note.md) | DELETE |  |
| [List Contact Notes](actions/list-contact-notes.md) | GET |  |
| [Update Contact Note](actions/update-contact-note.md) | PUT |  |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST |  |
| [Create Message](actions/create-message.md) | POST |  |
| [Get Conversation](actions/get-conversation.md) | GET |  |
| [List Conversations](actions/list-conversations.md) | GET |  |
| [Update Conversation](actions/update-conversation.md) | PUT |  |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST |  |
| [Get Incident](actions/get-incident.md) | GET |  |
| [List Incidents](actions/list-incidents.md) | GET |  |
| [Update Incident](actions/update-incident.md) | PUT |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Summary Report](actions/get-channel-summary-report.md) | GET |  |
| [Get Response Time Report](actions/get-response-time-report.md) | GET |  |
| [Get Staff Report](actions/get-staff-report.md) | GET |  |
| [Get Tags Report](actions/get-tags-report.md) | GET |  |
| [Get Volume Report](actions/get-volume-report.md) | GET |  |

### Response Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Response Template](actions/create-response-template.md) | POST |  |
| [Get Response Template](actions/get-response-template.md) | GET |  |
| [List Response Templates](actions/list-response-templates.md) | GET |  |
| [Update Response Template](actions/update-response-template.md) | PUT |  |

### Satisfaction Rating

| Action | Method | Description |
| --- | --- | --- |
| [List Satisfaction Ratings](actions/list-satisfaction-ratings.md) | GET |  |

### Staff User

| Action | Method | Description |
| --- | --- | --- |
| [Create Staff](actions/create-staff.md) | POST |  |
| [List Staff](actions/list-staff.md) | GET |  |

### System

| Action | Method | Description |
| --- | --- | --- |
| [List Systems](actions/list-systems.md) | GET |  |

