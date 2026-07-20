# WhatsBox: List Webhook Subscriptions

Retrieves all webhook subscriptions from WhatsBox.

```
GET https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-webhook-subscriptions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "platform": "string",
      "status": "string",
      "subscriberReferenceId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `platform` | string |  |
| `status` | string |  |
| `subscriberReferenceId` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `GET /webhook-subscriptions` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

