# <img src="https://images.mindcloud.co/apps/icons/bytebot_1776256282765.png" alt="bytebot logo" width="28" height="28"> bytebot: Universal API

Bytebot is a self-hosted AI desktop agent that exposes task-management and desktop-control APIs for automating work on a virtual desktop.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bytebot/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bytebot.ai
- **Vendor API docs:** https://docs.bytebot.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytebot/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from bytebot. |

