# Better Stack Telemetry: Update Source Group

Updates an existing source group in Better Stack Telemetry.

```
PUT https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceGroupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/update-source-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceGroupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceGroupId` | string | yes | ID of the source group to update |
| `name` | string | no | Source group name |
| `sortIndex` | number | no | Sort order index for the source group |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `PATCH /api/v1/source-groups/:source_group_id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source-group.md) for the provider-specific parameters and requirements.

