# Timetoreply: List Agent Alerts



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-agent-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-agent-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "agentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-agent-alerts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | number | yes | Agent identifier from the alert route. |
| `days` | number | no | Number of days of alerts to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mailbox_list": {},
      "messages": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mailbox_list` | object |  |
| `messages` | object |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/reports/alerts/:agent_id` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agent-alerts.md) for the provider-specific parameters and requirements.

