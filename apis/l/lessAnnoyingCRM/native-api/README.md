# Less Annoying CRM: Native API Reference

A consolidated summary of Less Annoying CRM's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://account.lessannoyingcrm.com/api_docs/v2/Getting_Started/Introduction
- **API base URL:** `https://api.lessannoyingcrm.com/v2`

## Authentication

### API Key

Connect with a Less Annoying CRM API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://account.lessannoyingcrm.com/api_docs/v2/Getting_Started/Connect)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-CreateContact) |
| [Create Event](actions/create-event.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-CreateEvent) |
| [Create Note](actions/create-note.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-CreateNote) |
| [Create Pipeline Item](actions/create-pipeline-item.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-CreatePipelineItem) |
| [Create Task](actions/create-task.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-CreateTask) |
| [Get Contact](actions/get-contact.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-GetContact) |
| [Get Event](actions/get-event.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-GetEvent) |
| [Get Pipeline Item](actions/get-pipeline-item.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-GetPipelineItem) |
| [Get Task](actions/get-task.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-GetTask) |
| [Get User](actions/get-user.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Users#Goto-GetUser) |
| [List Calendars](actions/list-calendars.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Calendars#Goto-GetCalendars) |
| [List Events](actions/list-events.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-GetEvents) |
| [List Notes](actions/list-notes.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-GetNotes) |
| [List Pipeline Items](actions/list-pipeline-items.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-GetPipelineItems) |
| [List Pipeline Statuses](actions/list-pipeline-statuses.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Pipeline_Statuses#Goto-GetPipelineStatuses) |
| [List Pipelines](actions/list-pipelines.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Pipelines#Goto-GetPipelines) |
| [List Tasks](actions/list-tasks.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-GetTasks) |
| [List Users](actions/list-users.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Settings_Functions/Users#Goto-GetUsers) |
| [Search Contacts](actions/search-contacts.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-GetContacts) |
| [Update Contact](actions/update-contact.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-EditContact) |
| [Update Event](actions/update-event.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Events#Goto-EditEvent) |
| [Update Note](actions/update-note.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-EditNote) |
| [Update Pipeline Item](actions/update-pipeline-item.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Pipeline_Items#Goto-EditPipelineItem) |
| [Update Task](actions/update-task.md) | `POST /` | [docs](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Tasks#Goto-EditTask) |
