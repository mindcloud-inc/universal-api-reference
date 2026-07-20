# Meetstream AI: Disable Cron

Updates calendar auto-scheduling in Meetstream AI.

```
PUT https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/disable-cron
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/disable-cron" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/disable-cron', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_schedule_enabled": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_schedule_enabled` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Meetstream AI API, this operation is `POST /calendar/auto-schedule/disable` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-cron.md) for the provider-specific parameters and requirements.

