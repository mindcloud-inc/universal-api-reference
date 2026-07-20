# <img src="https://images.mindcloud.co/apps/icons/postman_1774544156141.png" alt="Postman logo" width="28" height="28"> Postman: Universal API

Manage Postman workspaces, environments, monitors, and mock servers through the Postman API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postman/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postman.com/
- **Vendor API docs:** https://learning.postman.com/docs/developer/postman-api/intro-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in Postman. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from Postman. |
| [Get Environment](actions/get-environment.md) | GET | Retrieves details for an environment from Postman. |
| [List Environments](actions/list-environments.md) | GET | Retrieves all accessible environments from Postman. |
| [Update Environment](actions/update-environment.md) | PUT | Updates an existing environment in Postman. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a new monitor in Postman. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes an existing monitor from Postman. |
| [Get Monitor](actions/get-monitor.md) | GET | Retrieves details for a monitor from Postman. |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves all available monitors from Postman. |
| [Run Monitor](actions/run-monitor.md) | POST | Runs an existing monitor in Postman. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in Postman. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Mock Server](actions/create-mock-server.md) | POST | Creates a new mock server in Postman. |
| [Delete Mock Server](actions/delete-mock-server.md) | DELETE | Deletes an existing mock server from Postman. |
| [Get Mock Server](actions/get-mock-server.md) | GET | Retrieves details for a mock server from Postman. |
| [List Mock Server Call Logs](actions/list-mock-server-call-logs.md) | GET | Retrieves call logs for a mock server in Postman. |
| [List Mock Servers](actions/list-mock-servers.md) | GET | Retrieves all mock servers from Postman. |
| [Publish Mock Server](actions/publish-mock-server.md) | PUT | Sets a mock server to public in Postman. |
| [Unpublish Mock Server](actions/unpublish-mock-server.md) | PUT | Sets a mock server to private in Postman. |
| [Update Mock Server](actions/update-mock-server.md) | PUT | Updates an existing mock server in Postman. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves authenticated user details and usage limits from Postman. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Postman. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from Postman. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves details for a workspace from Postman. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves all accessible workspaces from Postman. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in Postman. |

