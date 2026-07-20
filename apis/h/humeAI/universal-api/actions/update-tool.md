# Hume AI: Update Tool



```
PUT https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/update-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/update-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/update-tool', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Tool ID. |
| `name` | string | yes | Updated tool name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hume AI API returns.

## Native endpoint

Through the native Hume AI API, this operation is `PATCH /v0/evi/tools/:id` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tool.md) for the provider-specific parameters and requirements.

