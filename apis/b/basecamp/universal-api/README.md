# <img src="https://images.mindcloud.co/apps/icons/icon_1773154958886.jpeg" alt="Basecamp logo" width="28" height="28"> Basecamp: Universal API

Manage projects, messages, schedules, and files in Basecamp

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/basecamp/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://basecamp.com
- **Vendor API docs:** https://github.com/basecamp/bc3-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authorization](actions/get-authorization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorization](actions/get-authorization.md) | GET | Retrieves authorization details and accessible accounts from Basecamp. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in a Basecamp vault. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Basecamp. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from a Basecamp vault. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message on a Basecamp message board. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Basecamp. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from a Basecamp message board. |

### Message Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Message Board](actions/get-message-board.md) | GET | Retrieves a message board from Basecamp. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Basecamp. |
| [List People](actions/list-people.md) | GET | Retrieves all people from Basecamp. |
| [List Project People](actions/list-project-people.md) | GET | Retrieves people for a project in Basecamp. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Basecamp. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all visible projects from Basecamp. |

### Recording

| Action | Method | Description |
| --- | --- | --- |
| [List Recordings](actions/list-recordings.md) | GET | Retrieves recordings from Basecamp. |
| [Search Recordings](actions/search-recordings.md) | GET | Finds recordings in Basecamp by search query. |

### Todo

| Action | Method | Description |
| --- | --- | --- |
| [Complete Todo](actions/complete-todo.md) | PUT | Marks a to-do as completed in Basecamp. |
| [Create Todo](actions/create-todo.md) | POST | Creates a new to-do in a Basecamp to-do list. |
| [Get Todo](actions/get-todo.md) | GET | Retrieves a to-do from Basecamp. |
| [List Todos](actions/list-todos.md) | GET | Retrieves to-dos from a Basecamp to-do list. |

### Todolist

| Action | Method | Description |
| --- | --- | --- |
| [Create Todolist](actions/create-todolist.md) | POST | Creates a new to-do list in a Basecamp to-do set. |
| [Get Todolist](actions/get-todolist.md) | GET | Retrieves a to-do list from Basecamp. |
| [List Todolists](actions/list-todolists.md) | GET | Retrieves to-do lists from a Basecamp to-do set. |

### Todoset

| Action | Method | Description |
| --- | --- | --- |
| [Get Todoset](actions/get-todoset.md) | GET | Retrieves a to-do set from Basecamp. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [List Uploads](actions/list-uploads.md) | GET | Retrieves uploads from a Basecamp vault. |

