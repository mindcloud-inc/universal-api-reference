# Chatvolt AI: Enable/Disable Agent Integration

Enables or disables an agent integration in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "type": "string",
  "enabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "type": "string",
    "enabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the agent to which the service provider belongs. |
| `type` | string | yes | Type of the service provider for which the webhook status will be changed. |
| `enabled` | boolean | yes | Defines the new webhook status. `true` to enable, `false` to disable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Response payload. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PATCH /agents/{id}/webhook` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-webhook.md) for the provider-specific parameters and requirements.

