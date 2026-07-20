# Attio: List Webhooks

Retrieves webhooks from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-webhooks?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "status": "string",
      "subscriptions": [
        {}
      ],
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the webhook was created. |
| `id` | object | Webhook identifier payload containing workspace and webhook ids. |
| `status` | string | Webhook status. |
| `subscriptions` | array<object> | Webhook subscription definitions. |
| `targetUrl` | string | Destination URL for webhook deliveries. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/webhooks` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

