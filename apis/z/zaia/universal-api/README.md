# <img src="https://images.mindcloud.co/apps/icons/zaia_1776266924181.png" alt="Zaia logo" width="28" height="28"> Zaia: Universal API

Manage AI agents, squads, workflows, channels, and support

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zaia/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zaia.app/en
- **Vendor API docs:** https://docs.zaia.app

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agents](actions/list-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from your Zaia workspace. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves channels from your Zaia workspace. |

### Component

| Action | Method | Description |
| --- | --- | --- |
| [List Components](actions/list-components.md) | GET | Retrieves components from your Zaia workspace. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from your Zaia workspace. |

### Datagrid

| Action | Method | Description |
| --- | --- | --- |
| [List Datagrids](actions/list-datagrids.md) | GET | Retrieves datagrids from your Zaia workspace. |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from your Zaia workspace. |

### Execution

| Action | Method | Description |
| --- | --- | --- |
| [List Executions](actions/list-executions.md) | GET | Retrieves executions from your Zaia workspace. |

### External User

| Action | Method | Description |
| --- | --- | --- |
| [List External Users](actions/list-external-users.md) | GET | Retrieves external users from your Zaia workspace. |

### Llm Provider

| Action | Method | Description |
| --- | --- | --- |
| [List LLM Providers](actions/list-llm-providers.md) | GET | Retrieves LLM providers from your Zaia workspace. |

### Llm Provider Option

| Action | Method | Description |
| --- | --- | --- |
| [List LLM Provider Options](actions/list-llm-provider-options.md) | GET | Retrieves LLM provider options from your Zaia workspace. |

### Mcp

| Action | Method | Description |
| --- | --- | --- |
| [List MCPs](actions/list-mcps.md) | GET | Retrieves MCPs from your Zaia workspace. |

### Mcp Option

| Action | Method | Description |
| --- | --- | --- |
| [List MCP Options](actions/list-mcp-options.md) | GET | Retrieves MCP options from your Zaia workspace. |

### Responder

| Action | Method | Description |
| --- | --- | --- |
| [List Responders](actions/list-responders.md) | GET | Retrieves responder identities from your Zaia workspace. |

### Squad

| Action | Method | Description |
| --- | --- | --- |
| [List Squads](actions/list-squads.md) | GET | Retrieves squads from your Zaia workspace. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Zaia. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Zaia. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from your Zaia workspace. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from your Zaia workspace. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Zaia. |

### Ticketing Team

| Action | Method | Description |
| --- | --- | --- |
| [List Ticketing Teams](actions/list-ticketing-teams.md) | GET | Retrieves ticketing teams from your Zaia workspace. |

