# eGain: Update Authentication

Updates an existing authentication in eGain.

```
PUT https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-authentication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "basicAuth.password": "string",
  "basicAuth.username": "Ava Chen",
  "id": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-authentication', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "basicAuth.password": "string",
    "basicAuth.username": "Ava Chen",
    "id": "string",
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `basicAuth.password` | string | yes | Basic auth password. |
| `basicAuth.username` | string | yes | Basic auth username. |
| `id` | string | yes | Authentication ID. |
| `name` | string | yes | Authentication name. |
| `type` | string | yes | Authentication type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `PUT /authentications/:id` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-authentication.md) for the provider-specific parameters and requirements.

