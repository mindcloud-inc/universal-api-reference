# CallTrackingMetrics: Create Tracking Source

Creates a new tracking source in CallTrackingMetrics.

```
POST https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-tracking-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-tracking-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/create-tracking-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the tracking source. |
| `description` | string | no | An optional description for the tracking source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "source": {
        "accountId": 1,
        "defaultCost": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "online": true,
        "position": 1
      },
      "url": "https://example.com",
      "warnings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `source` | object |  |
| `source.accountId` | number |  |
| `source.defaultCost` | string |  |
| `source.description` | string |  |
| `source.id` | string |  |
| `source.name` | string |  |
| `source.online` | boolean |  |
| `source.position` | number |  |
| `url` | string |  |
| `warnings` | object |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `POST /accounts/:accountId/sources.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracking-source.md) for the provider-specific parameters and requirements.

