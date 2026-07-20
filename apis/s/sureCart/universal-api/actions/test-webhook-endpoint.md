# SureCart: Test Webhook Endpoint



```
PUT https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/test-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/test-webhook-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "012f238f-1b66-4a1d-b5ff-2b1793e4d08c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/test-webhook-endpoint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "012f238f-1b66-4a1d-b5ff-2b1793e4d08c"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The webhook endpoint ID to test. Example: `012f238f-1b66-4a1d-b5ff-2b1793e4d08c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automationService": "string",
      "createdAt": 1,
      "description": "string",
      "enabled": true,
      "erroringGracePeriodEndsAt": 1,
      "erroringGracePeriodStartedAt": 1,
      "id": "string",
      "object": "string",
      "signingSecret": "string",
      "updatedAt": 1,
      "url": "https://example.com",
      "webhookEvents": [
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
| `automationService` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `erroringGracePeriodEndsAt` | number |  |
| `erroringGracePeriodStartedAt` | number |  |
| `id` | string |  |
| `object` | string |  |
| `signingSecret` | string |  |
| `updatedAt` | number |  |
| `url` | string |  |
| `webhookEvents` | array<string> |  |

## Native endpoint

Through the native SureCart API, this operation is `POST v1/webhook_endpoints/:id/test` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-webhook-endpoint.md) for the provider-specific parameters and requirements.

