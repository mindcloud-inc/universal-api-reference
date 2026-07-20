# SureCart: Retrieve Webhook Endpoint



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-webhook-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-webhook-endpoint?connectionId=$CONNECTION_ID&id=012f238f-1b66-4a1d-b5ff-2b1793e4d08c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "012f238f-1b66-4a1d-b5ff-2b1793e4d08c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-webhook-endpoint?${params}`, {
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
| `id` | string | yes | The webhook endpoint ID to retrieve. Example: `012f238f-1b66-4a1d-b5ff-2b1793e4d08c`. |

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

Through the native SureCart API, this operation is `GET v1/webhook_endpoints/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook-endpoint.md) for the provider-specific parameters and requirements.

