# LLMWhisperer: Delete Webhook Endpoint

Deletes an existing webhook endpoint from LLMWhisperer.

```
DELETE https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/delete-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/delete-webhook-endpoint?connectionId=$CONNECTION_ID&webhookName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/delete-webhook-endpoint?${params}`, {
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
| `webhookName` | string | yes | Webhook name to delete. |

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

Through the native LLMWhisperer API, this operation is `DELETE /whisper-manage-callback` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-endpoint.md) for the provider-specific parameters and requirements.

