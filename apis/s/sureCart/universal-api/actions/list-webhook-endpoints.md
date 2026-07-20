# SureCart: List Webhook Endpoints



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-webhook-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-webhook-endpoints?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-webhook-endpoints?${params}`, {
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

Through the native SureCart API, this operation is `GET v1/webhook_endpoints` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-endpoints.md) for the provider-specific parameters and requirements.

