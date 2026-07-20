# Statsig: Update a metric

Updates a metric in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-a-metric-post-console-v1-metrics-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-a-metric-post-console-v1-metrics-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-a-metric-post-console-v1-metrics-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `name` | string | no | Request body field. |
| `description` | string | no | Request body field. |
| `tags` | list | no | Request body field. |
| `isVerified` | boolean | no | Request body field. |
| `isReadOnly` | boolean | no | Request body field. |
| `isPermanent` | boolean | no | Request body field. |
| `warehouseNative` | object | no | Request body field. |
| `unitTypes` | list | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `directionality` | string | no | Request body field. |
| `dryRun` | boolean | no | Request body field. |
| `owner` | object | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/metrics/{id}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-metric-post-console-v1-metrics-id.md) for the provider-specific parameters and requirements.

