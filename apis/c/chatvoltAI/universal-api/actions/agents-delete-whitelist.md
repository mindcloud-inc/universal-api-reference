# Chatvolt AI: Delete Number from Whitelist

Deletes a whitelist number from Chatvolt AI.

```
DELETE https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-whitelist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-whitelist?connectionId=$CONNECTION_ID&id=string&whatsappNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "whatsappNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-whitelist?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the agent. |
| `whatsappNumber` | string | yes | The WhatsApp number to be removed from the whitelist. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Message. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `DELETE /agent-whitelist-whatsapp/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-delete-whitelist.md) for the provider-specific parameters and requirements.

