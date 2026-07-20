# <img src="https://images.mindcloud.co/apps/icons/cloud-cli_1775760164337.png" alt="Cloud CLI logo" width="28" height="28"> Cloud CLI: Universal API

Launch, share, and manage cloud coding environments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudCLI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudcli.ai
- **Vendor API docs:** https://developer.cloudcli.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List AI Agent Models](actions/list-ai-agent-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudCLI/latest/actions/list-ai-agent-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in Cloud CLI. |
| [Delete Environment](actions/delete-environment.md) | DELETE | Deletes an existing environment from Cloud CLI. |
| [Get Environment](actions/get-environment.md) | GET | Retrieves an environment from Cloud CLI. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from Cloud CLI. |
| [Start Environment](actions/start-environment.md) | PUT | Starts an existing environment in Cloud CLI. |
| [Stop Environment](actions/stop-environment.md) | PUT | Stops an existing environment in Cloud CLI. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [List AI Agent Models](actions/list-ai-agent-models.md) | GET | Retrieves supported AI agent models from Cloud CLI. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get SSH Credentials](actions/get-ssh-credentials.md) | GET | Retrieves SSH credentials for a Cloud CLI environment. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Execute AI Agent](actions/execute-ai-agent.md) | POST | Runs an AI agent in a Cloud CLI environment. |

