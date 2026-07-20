# <img src="https://images.mindcloud.co/apps/icons/echowin_1774455127728.png" alt="echowin logo" width="28" height="28"> echowin: Universal API

Manage contacts, calls, agents, and knowledge in echowin

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/echowin/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://echo.win
- **Vendor API docs:** https://echo.win/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echowin/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Instructions](actions/get-agent-instructions.md) | GET | Retrieves agent instructions from echowin. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from echowin. |
| [Update Agent Instructions](actions/update-agent-instructions.md) | PUT | Updates agent instructions in echowin. |

### Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact Assignments](actions/add-contact-assignments.md) | POST | Adds contact assignments in echowin. |
| [List Contact Assignments](actions/list-contact-assignments.md) | GET | Retrieves contact assignments from echowin. |
| [Replace Contact Assignments](actions/replace-contact-assignments.md) | PUT | Replaces contact assignments in echowin. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To Boards](actions/add-contact-to-boards.md) | POST | Adds a contact to boards in echowin. |
| [List Boards](actions/list-boards.md) | GET | Retrieves boards from echowin. |
| [Update Contact Boards](actions/update-contact-boards.md) | PUT | Updates contact boards in echowin. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from echowin. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from echowin. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | POST | Creates contacts in echowin in bulk. |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in echowin. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from echowin. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from echowin. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from echowin. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in echowin. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET | Retrieves contact custom fields from echowin. |

### Knowledgebase

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Knowledgebase](actions/get-agent-knowledgebase.md) | GET | Retrieves an agent knowledge base from echowin. |

### Knowledgebase Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Agent Knowledgebase](actions/search-agent-knowledgebase.md) | GET | Finds knowledge base entries in echowin by search query. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST | Creates a contact note in echowin. |
| [List Contact Notes](actions/list-contact-notes.md) | GET | Retrieves contact notes from echowin. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in echowin. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from echowin. |

