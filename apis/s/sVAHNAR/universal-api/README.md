# <img src="https://images.mindcloud.co/apps/icons/s-vahnar_1774881938331.png" alt="SVAHNAR logo" width="28" height="28"> SVAHNAR: Universal API

Build, deploy, and manage AI agents with SVAHNAR

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sVAHNAR/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.svahnar.com/
- **Vendor API docs:** https://docs.svahnar.com/docs/GetStarted/Overview/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Agent Configuration](actions/get-agent-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-configuration?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Delete Agent](actions/delete-agent.md) | DELETE | Deletes an existing agent from SVAHNAR. |
| [Delete Multiple Agents](actions/delete-multiple-agents.md) | DELETE | Deletes multiple agents from SVAHNAR. |
| [List All Agents](actions/list-all-agents.md) | GET | Retrieves all agents from SVAHNAR. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Configuration](actions/get-agent-configuration.md) | GET | Retrieves an agent configuration from SVAHNAR. |
| [Get Agent Details](actions/get-agent-details.md) | GET | Retrieves agent details from SVAHNAR. |
| [Get Credits](actions/get-credits.md) | GET |  |
| [Login](actions/login.md) | GET |  |
| [Run Agent](actions/run-agent.md) | POST | Runs an agent in SVAHNAR. |
| [Test Agent](actions/test-agent.md) | POST | Tests an agent in SVAHNAR. |
| [Validate Agent Configuration](actions/validate-agent-configuration.md) | GET | Validates an agent configuration in SVAHNAR. |

