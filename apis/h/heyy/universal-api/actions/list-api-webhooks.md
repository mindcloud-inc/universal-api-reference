# Heyy: List API Webhooks

Retrieves API webhooks from a Heyy workspace.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-api-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-api-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-api-webhooks?${params}`, {
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
      "id": "string",
      "isActive": true,
      "tenantId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
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
| `id` | string |  |
| `isActive` | boolean |  |
| `tenantId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /api_webhooks` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-webhooks.md) for the provider-specific parameters and requirements.

