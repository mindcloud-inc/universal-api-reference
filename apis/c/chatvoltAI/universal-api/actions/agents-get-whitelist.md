# Chatvolt AI: Get Whitelist Numbers

Retrieves whitelist numbers from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get-whitelist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get-whitelist?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-get-whitelist?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<string> | Response items. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /agent-whitelist-whatsapp/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-get-whitelist.md) for the provider-specific parameters and requirements.

