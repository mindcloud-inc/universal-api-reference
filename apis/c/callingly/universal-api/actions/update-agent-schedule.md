# Callingly: Update Agent Schedule

Updates an agent schedule in Callingly.

```
PUT https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-agent-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-agent-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "scheduleJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callingly/latest/actions/update-agent-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "scheduleJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `scheduleJson` | string | yes | Pass the full schedule array as JSON using the Get Agent Schedule response shape. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Callingly API returns.

## Native endpoint

Through the native Callingly API, this operation is `PUT /v1/agents/{{id}}/schedule` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent-schedule.md) for the provider-specific parameters and requirements.

