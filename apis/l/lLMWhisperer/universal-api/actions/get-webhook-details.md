# LLMWhisperer: Get Webhook Details

Retrieves a webhook endpoint from LLMWhisperer by name.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-webhook-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-webhook-details?connectionId=$CONNECTION_ID&webhookName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-webhook-details?${params}`, {
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
| `webhookName` | string | yes | Webhook name to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth_token": "string",
      "url": "https://example.com",
      "webhook_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth_token` | string |  |
| `url` | string |  |
| `webhook_name` | string |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /whisper-manage-callback` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-details.md) for the provider-specific parameters and requirements.

