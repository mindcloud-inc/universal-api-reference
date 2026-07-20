# <img src="https://images.mindcloud.co/apps/icons/logsnag-icon_1776187386479.png" alt="LogSnag logo" width="28" height="28"> LogSnag: Universal API

LogSnag is an event monitoring API for publishing logs, identifying users, and tracking numeric insights in real time.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logSnag/latest
- **Category:** IT Operations / Observability
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://logsnag.com
- **Vendor API docs:** https://docs.logsnag.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Group User](actions/group-user.md):

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "groupId": "string",
  "userId": "string"
}'
```

## Actions (6)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Group User](actions/group-user.md) | PUT |  |

### Insight

| Action | Method | Description |
| --- | --- | --- |
| [Mutate Insight](actions/mutate-insight.md) | PUT |  |
| [Publish Insight](actions/publish-insight.md) | POST |  |

### Log Event

| Action | Method | Description |
| --- | --- | --- |
| [Publish Log Event](actions/publish-log-event.md) | POST |  |

### Page View

| Action | Method | Description |
| --- | --- | --- |
| [Track Page View](actions/track-page-view.md) | POST |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Identify User](actions/identify-user.md) | PUT |  |

