# Timetoreply: List Alerts



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-alerts?${params}`, {
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
| `agent` | number | no | Agent identifier to filter alerts. |
| `days` | number | no | Number of days of alerts to include. |
| `team` | number | no | Team identifier to filter alerts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "handledMessages": {},
      "liveMessages": {},
      "mailbox_list": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `handledMessages` | object |  |
| `liveMessages` | object |  |
| `mailbox_list` | object |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/reports/alerts` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

