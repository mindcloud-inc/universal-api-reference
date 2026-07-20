# <img src="https://images.mindcloud.co/apps/icons/toolhouse_1774904105191.png" alt="Toolhouse logo" width="28" height="28"> Toolhouse: Universal API

Build, run, and manage Toolhouse AI agents and agent runs through the Toolhouse API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/toolhouse/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://toolhouse.ai
- **Vendor API docs:** https://docs.toolhouse.ai/toolhouse/agent-workers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Agent Runs](actions/list-agent-runs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Delete Schedule](actions/delete-schedule.md) | DELETE |  |
| [Get Schedule](actions/get-schedule.md) | GET |  |
| [List Schedules](actions/list-schedules.md) | GET |  |
| [Update Schedule](actions/update-schedule.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Continue Agent Run](actions/continue-agent-run.md) | PUT |  |
| [Convert Text to Cron](actions/convert-text-to-cron.md) | GET |  |
| [Create Agent Run](actions/create-agent-run.md) | POST |  |
| [Get Agent Run](actions/get-agent-run.md) | GET |  |
| [List Agent Runs](actions/list-agent-runs.md) | GET |  |

