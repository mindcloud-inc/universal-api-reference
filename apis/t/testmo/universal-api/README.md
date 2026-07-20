# <img src="https://images.mindcloud.co/apps/icons/testmo_1777036887110.png" alt="Testmo logo" width="28" height="28"> Testmo: Universal API

Manage Testmo projects, users, milestones, test runs, sessions, automation runs, cases, folders, and related QA workflows through the Testmo REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/testmo/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.testmo.com/
- **Vendor API docs:** https://docs.testmo.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [List Case Attachments](actions/list-case-attachments.md) | GET | Retrieves attachments for a test case in Testmo. |

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [List Cases](actions/list-cases.md) | GET | Retrieves cases for a project in Testmo. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [List Automation Sources](actions/list-automation-sources.md) | GET | Retrieves automation sources for a project in Testmo. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders for a project in Testmo. |

### Milestones

| Action | Method | Description |
| --- | --- | --- |
| [Get Milestone](actions/get-milestone.md) | GET | Retrieves milestone details from Testmo by ID. |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves milestones for a project in Testmo. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from Testmo by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all accessible projects from Testmo. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Session](actions/get-session.md) | GET | Retrieves session details from Testmo by ID. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves sessions for a project in Testmo. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Complete Automation Run](actions/complete-automation-run.md) | PUT | Marks an automation run as completed in Testmo. |
| [Create Automation Run](actions/create-automation-run.md) | POST | Creates a new automation run in Testmo. |
| [Get Automation Run](actions/get-automation-run.md) | GET | Retrieves automation run details from Testmo by ID. |
| [Get Run](actions/get-run.md) | GET | Retrieves run details from Testmo by ID. |
| [List Automation Runs](actions/list-automation-runs.md) | GET | Retrieves automation runs for a project in Testmo. |
| [List Runs](actions/list-runs.md) | GET | Retrieves runs for a project in Testmo. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Testmo. |
| [Get User](actions/get-user.md) | GET | Retrieves user details from Testmo by ID. |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves users for a project in Testmo. |
| [List Users](actions/list-users.md) | GET | Retrieves all available users from Testmo. |

