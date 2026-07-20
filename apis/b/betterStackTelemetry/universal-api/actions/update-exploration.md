# Better Stack Telemetry: Update Exploration

Updates an existing exploration in Better Stack Telemetry.

```
PUT https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "746510"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-exploration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "746510"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the exploration to update. Example: `746510`. |
| `name` | string | no | New exploration name. Example: `Log anomaly detection`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateRangeFrom` | string | no | Start of the exploration date range. Example: `now-3h`. |
| `dateRangeTo` | string | no | End of the exploration date range. Example: `now`. |
| `explorationGroupId` | number | no | Exploration group ID for the exploration. Example: `1234`. |
| `chart` | object | no | Chart configuration object. |
| `queries[]` | array | no | Array of exploration queries. |
| `variables[]` | array | no | Array of exploration variables. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `PATCH /api/v2/explorations/:id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-exploration.md) for the provider-specific parameters and requirements.

