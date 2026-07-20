# <img src="https://images.mindcloud.co/apps/icons/make_1776267481211.png" alt="Make logo" width="28" height="28"> Make: Universal API

Make is a visual workflow automation platform for building and managing automations, AI agents, and integrations across business systems.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/make/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.make.com/en
- **Vendor API docs:** https://developers.make.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Authorization](actions/get-current-authorization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/make/latest/actions/get-current-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Ai Agent

| Action | Method | Description |
| --- | --- | --- |
| [List AI Agents](actions/list-ai-agents.md) | GET | Lists AI agents for the specified team. |

### Authorization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Authorization](actions/get-current-authorization.md) | GET | Returns current authorization details for the authenticated user, including the token scopes and authentication method used. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET | Lists connections for the specified team. |

### Credential Request

| Action | Method | Description |
| --- | --- | --- |
| [List Credential Requests](actions/list-credential-requests.md) | GET | Lists credential requests for the specified team. |

### Custom Property Structure

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Property Structures](actions/list-custom-property-structures.md) | GET | Lists custom property structures for the specified organization. |

### Data Store

| Action | Method | Description |
| --- | --- | --- |
| [List Data Stores](actions/list-data-stores.md) | GET | Lists data stores for the specified team. |

### Data Structure

| Action | Method | Description |
| --- | --- | --- |
| [List Data Structures](actions/list-data-structures.md) | GET | Lists data structures for the specified team. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Lists devices for the specified team. |

### Hook

| Action | Method | Description |
| --- | --- | --- |
| [List Hooks](actions/list-hooks.md) | GET | Lists hooks for the specified team. |

### Key

| Action | Method | Description |
| --- | --- | --- |
| [List Keys](actions/list-keys.md) | GET | Lists keys in the specified team's custom keychain. |

### Llm Provider

| Action | Method | Description |
| --- | --- | --- |
| [List LLM Providers](actions/list-llm-providers.md) | GET | Lists LLM providers for the specified team. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Lists notifications for the authenticated user. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Lists the organizations where the authenticated user is a member. |

### Scenario

| Action | Method | Description |
| --- | --- | --- |
| [List Scenarios](actions/list-scenarios.md) | GET | Lists scenarios for the specified team. |

### Scenario Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Scenario Folder](actions/create-scenario-folder.md) | POST | Creates a scenario folder in the specified team. |
| [List Scenario Folders](actions/list-scenario-folders.md) | GET | Lists scenario folders for the specified team. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Lists the teams in the specified organization. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Lists templates for the specified team. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Returns details for the authenticated user. |

### User Role

| Action | Method | Description |
| --- | --- | --- |
| [List User Roles](actions/list-user-roles.md) | GET | Lists available user role definitions, including role IDs and names. |

