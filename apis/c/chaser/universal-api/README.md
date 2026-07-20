# <img src="https://images.mindcloud.co/apps/icons/unnamed-10_1774869646537.png" alt="Chaser logo" width="28" height="28"> Chaser: Universal API

Chaser manages Slack-scoped task lists for the connected workspace, exposing task retrieval and later task CRUD/command workflows through the Chaser task API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chaser/latest
- **Category:** Communication / Team Messaging
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://appsmindcloud.slack.com
- **Vendor API docs:** https://www.trychaser.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaser/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Chaser. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Chaser. |

