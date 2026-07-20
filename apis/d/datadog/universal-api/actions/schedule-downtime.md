# Datadog: Schedule Downtime

Creates a new downtime in Datadog.

```
POST https://connect.mindcloud.co/v1/universal/datadog/latest/actions/schedule-downtime
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/schedule-downtime" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/schedule-downtime', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | JSON:API downtime payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "included": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Downtime record returned by the create request. |
| `included` | array<object> | Related resources included by the response. |

## Native endpoint

Through the native Datadog API, this operation is `POST /api/v2/downtime` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-downtime.md) for the provider-specific parameters and requirements.

