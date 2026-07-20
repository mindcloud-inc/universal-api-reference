# <img src="https://images.mindcloud.co/apps/icons/testomato_1776111403452.png" alt="Testomato logo" width="28" height="28"> Testomato: Universal API

Testomato REST API wrapper for website monitoring, project management, and check results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/testomato/latest
- **Category:** IT Operations / Observability
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.testomato.com
- **Vendor API docs:** https://help.testomato.com/api/testomato-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API token](actions/verify-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get API token](actions/get-api-token.md) | POST | Generates an API token in Testomato. |
| [Verify API token](actions/verify-api-token.md) | GET | Verifies an API token in Testomato. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Get test](actions/get-test.md) | GET | Retrieves a test from Testomato. |
| [Start project group](actions/start-project-group.md) | GET | Starts a project group of checks in Testomato. |
| [Uptime](actions/uptime.md) | GET | Retrieves project uptime data from Testomato. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Add user to project](actions/add-user-to-project.md) | POST | Adds a user to a Testomato project. |
| [Get project](actions/get-project.md) | GET | Retrieves a project from Testomato. |
| [New project](actions/new-project.md) | POST | Creates a new project in Testomato. |
| [Project delete](actions/project-delete.md) | DELETE | Deletes an existing project from Testomato. |
| [Project groups](actions/project-groups.md) | GET | Retrieves project groups from Testomato. |
| [Project notifications](actions/project-notifications.md) | GET | Retrieves project notification settings from Testomato. |
| [Project permissions](actions/project-permissions.md) | GET | Retrieves project permissions from Testomato. |
| [Project results](actions/project-results.md) | GET | Retrieves project check results from Testomato. |
| [Project roles](actions/project-roles.md) | GET | Retrieves project roles from Testomato. |
| [Project status](actions/project-status.md) | GET | Retrieves project status from Testomato. |
| [Project update](actions/project-update.md) | PUT | Updates an existing project in Testomato. |
| [Project users](actions/project-users.md) | GET | Retrieves project users from Testomato. |
| [Response times](actions/response-times.md) | GET | Retrieves project response times from Testomato. |
| [Simplified project status](actions/simplified-project-status.md) | GET | Retrieves simplified project status from Testomato. |
| [Starting project](actions/starting-project.md) | GET | Starts all checks in a Testomato project. |
| [Update notifications](actions/update-notifications.md) | PUT | Updates project notification settings in Testomato. |

