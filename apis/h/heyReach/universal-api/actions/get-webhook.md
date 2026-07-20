# Hey Reach: Get Webhook

Retrieves a webhook from Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignIds": [
        1
      ],
      "eventType": "string",
      "id": 1,
      "isActive": true,
      "webhookName": "Ava Chen",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignIds` | array<number> |  |
| `eventType` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `webhookName` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `GET /api/public/webhooks/GetWebhookById` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

