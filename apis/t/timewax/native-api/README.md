# Timewax: Native API Reference

A consolidated summary of Timewax's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://timewax.atlassian.net/servicedesk/customer/portal/7/topic/a7c3f08f-024f-4dc1-9484-a92c06be3724
- **API base URL:** `https://api.timewax.com/`

## Authentication

### Timewax Credentials

Use Timewax client environment, API ID username, and password to obtain a short-lived API token for XML API services.

### Credentials

- **Client:** `client` · required · Timewax client environment name from the top-right settings menu.
- **API ID:** `username` · required · Timewax API ID from Masters > Resources > selected resource > Data Security tab > API ID. This maps to the Timewax XML <username> field.
- **Password:** `password` · required · Password for the Timewax API user.

[Official authentication documentation](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230681619)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml, text/xml` |
| `Content-Type` | `application/xml` |

Responses from this API use XML. Response data is read from `response`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST company/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230878315) |
| [Create Department](actions/create-department.md) | `POST department/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230878382) |
| [Create Planning Booking](actions/create-planning-booking.md) | `POST calendar/entries/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231632128) |
| [Create Position](actions/create-position.md) | `POST position/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231468168) |
| [Create Project](actions/create-project.md) | `POST project/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231599173) |
| [Create Project Activity](actions/create-project-activity.md) | `POST project/breakdown/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231631983) |
| [Create Resource](actions/create-resource.md) | `POST resource/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566461) |
| [Create Time Entry](actions/create-time-entry.md) | `POST time/entries/add/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664899) |
| [Get Authentication Token](actions/get-authentication-token.md) | `POST authentication/token/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230681619) |
| [Get Client](actions/get-client.md) | `POST company/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231370029) |
| [Get Department](actions/get-department.md) | `POST department/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231370079) |
| [Get Project](actions/get-project.md) | `POST project/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231631941) |
| [Get Project Activity](actions/get-project-activity.md) | `POST project/breakdown/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664770) |
| [Get Resource](actions/get-resource.md) | `POST resource/get/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664819) |
| [List Changed Planning Bookings](actions/list-changed-planning-bookings.md) | `POST calendar/entries/list_changed/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566556) |
| [List Changed Projects](actions/list-changed-projects.md) | `POST project/list_changed/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664714) |
| [List Clients](actions/list-clients.md) | `POST company/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231468145) |
| [List Departments](actions/list-departments.md) | `POST department/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2261811201) |
| [List Inactive Projects](actions/list-inactive-projects.md) | `POST project/list_inactive/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231599209) |
| [List Planning Bookings](actions/list-planning-bookings.md) | `POST calendar/entries/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664838) |
| [List Project Activities](actions/list-project-activities.md) | `POST project/breakdown/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566408) |
| [List Projects](actions/list-projects.md) | `POST project/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231664737) |
| [List Resources](actions/list-resources.md) | `POST resource/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566521) |
| [List Time Entries](actions/list-time-entries.md) | `POST time/entries/list/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566586) |
| [Update Client](actions/update-client.md) | `POST company/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2230878328) |
| [Update Department](actions/update-department.md) | `POST department/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231370086) |
| [Update Position](actions/update-position.md) | `POST position/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2259681281) |
| [Update Project](actions/update-project.md) | `POST project/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231599232) |
| [Update Project Activity](actions/update-project-activity.md) | `POST project/breakdown/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566418) |
| [Update Resource](actions/update-resource.md) | `POST resource/edit/` | [docs](https://timewax.atlassian.net/rest/servicedesk/knowledgebase/latest/articles/view/2231566471) |
