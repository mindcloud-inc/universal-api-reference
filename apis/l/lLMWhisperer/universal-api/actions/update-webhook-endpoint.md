# LLMWhisperer: Update Webhook Endpoint

Updates an existing webhook endpoint in LLMWhisperer.

```
PUT https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/update-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/update-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "authToken": "string",
  "webhookName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/update-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "authToken": "string",
    "webhookName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Updated callback URL to invoke after conversion completes. |
| `authToken` | string | yes | Updated bearer token sent by LLMWhisperer when invoking the webhook. |
| `webhookName` | string | yes | Existing webhook name to update. |

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
| `message` | string |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `PUT /whisper-manage-callback` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-endpoint.md) for the provider-specific parameters and requirements.

