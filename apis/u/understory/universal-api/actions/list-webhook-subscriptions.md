# Understory: List Webhook Subscriptions

Retrieves webhook subscriptions from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-webhook-subscriptions?${params}`, {
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
      "items": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "event_types": [
            [
              "string"
            ]
          ],
          "id": "string",
          "state": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].created_at` | date |  |
| `items[].event_types[]` | array<string> |  |
| `items[].id` | string |  |
| `items[].state` | string |  |
| `items[].updated_at` | date |  |
| `items[].url` | string |  |
| `next` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/webhook-subscriptions` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

