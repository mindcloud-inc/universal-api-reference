# Figma: Delete Webhook

Deletes an existing webhook from Figma.

```
DELETE https://connect.mindcloud.co/v1/universal/figma/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/figma/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&webhook_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhook_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/delete-webhook?${params}`, {
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
| `webhook_id` | string | yes | Webhook identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "context": "string",
      "contextId": "string",
      "description": "string",
      "endpoint": "string",
      "eventType": "string",
      "id": "string",
      "passcode": "string",
      "planApiId": "string",
      "status": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `context` | string |  |
| `contextId` | string |  |
| `description` | string |  |
| `endpoint` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `passcode` | string |  |
| `planApiId` | string |  |
| `status` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Figma API, this operation is `DELETE https://api.figma.com/v2/webhooks/:webhook_id` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

