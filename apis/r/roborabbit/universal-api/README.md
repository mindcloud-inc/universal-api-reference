# <img src="https://images.mindcloud.co/apps/icons/roborabbit_1774295210696.png" alt="Roborabbit logo" width="28" height="28"> Roborabbit: Universal API

Run browser automation tasks and retrieve task outputs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/roborabbit/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.roborabbit.com
- **Vendor API docs:** https://developers.roborabbit.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account status and quota usage from Roborabbit. |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves custom task feeds from Roborabbit. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Run](actions/create-run.md) | POST | Creates a new run for a Roborabbit task. |
| [List Runs](actions/list-runs.md) | GET | Retrieves runs for a specific Roborabbit task. |
| [Retrieve Run](actions/retrieve-run.md) | GET | Retrieves a run for a specific Roborabbit task. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves browser automation tasks from Roborabbit. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a browser automation task from Roborabbit. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | GET |  |

