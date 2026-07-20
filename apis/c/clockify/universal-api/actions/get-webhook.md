# Clockify: Get Webhook

Retrieves a specific webhook from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook?connectionId=$CONNECTION_ID&workspaceId=string&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-webhook?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `webhookId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authToken": "string",
      "deliveryEnabled": true,
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "triggerSource": [
        [
          "string"
        ]
      ],
      "triggerSourceType": "string",
      "url": "https://example.com",
      "userId": "string",
      "webhookEvent": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string |  |
| `deliveryEnabled` | boolean |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `triggerSource[]` | array<string> |  |
| `triggerSourceType` | string |  |
| `url` | string |  |
| `userId` | string |  |
| `webhookEvent` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/webhooks/:webhookId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

