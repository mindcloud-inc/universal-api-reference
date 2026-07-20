# <img src="https://images.mindcloud.co/apps/icons/beyond-presence-icon_1777055910855.png" alt="Beyond Presence logo" width="28" height="28"> Beyond Presence: Universal API

Manage Beyond Presence agents, avatars, calls, and external API configs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beyondPresence/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://beyondpresence.ai
- **Vendor API docs:** https://docs.bey.dev/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Beyond Presence. |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from Beyond Presence. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Beyond Presence. |
| [List Agents](actions/list-agents.md) | GET | Retrieves available agents from Beyond Presence. |
| [Update Agent](actions/update-agent.md) | PUT | Updates an existing agent in Beyond Presence. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies a Beyond Presence API key. |

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar](actions/get-avatar.md) | GET | Retrieves an avatar from Beyond Presence. |
| [List Avatars](actions/list-avatars.md) | GET | Retrieves available avatars from Beyond Presence. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Create Call](actions/create-call.md) | POST | Creates a new call in Beyond Presence. |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Beyond Presence. |
| [List Calls](actions/list-calls.md) | GET | Retrieves agent-managed calls from Beyond Presence. |

### Call Message

| Action | Method | Description |
| --- | --- | --- |
| [List Call Messages](actions/list-call-messages.md) | GET | Retrieves transcribed messages from a Beyond Presence call. |

### External Api Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Create External API Configuration](actions/create-external-api-configuration.md) | POST | Creates a new external API configuration in Beyond Presence. |
| [Delete External API Configuration](actions/delete-external-api-configuration.md) | DELETE | Deletes an external API configuration from Beyond Presence. |
| [Get External API Configuration](actions/get-external-api-configuration.md) | GET | Retrieves an external API configuration from Beyond Presence. |
| [List External API Configurations](actions/list-external-api-configurations.md) | GET | Retrieves external API configurations from Beyond Presence. |

