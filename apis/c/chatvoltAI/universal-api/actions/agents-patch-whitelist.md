# Chatvolt AI: Update Number in Whitelist

Updates a whitelist number in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-patch-whitelist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-patch-whitelist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "oldWhatsappNumber": "string",
  "newWhatsappNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-patch-whitelist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "oldWhatsappNumber": "string",
    "newWhatsappNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the agent. |
| `oldWhatsappNumber` | string | yes | The current WhatsApp number in the whitelist. |
| `newWhatsappNumber` | string | yes | The new WhatsApp number to replace the old one. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "whatsappNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | The ID of the agent. |
| `whatsappNumber` | string | The whitelisted WhatsApp number. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PATCH /agent-whitelist-whatsapp/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-patch-whitelist.md) for the provider-specific parameters and requirements.

