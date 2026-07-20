# Content Snare: List Webhooks

Retrieves webhooks from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-webhooks?${params}`, {
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
      "enabled": true,
      "id": "string",
      "subscriptions": [
        [
          "string"
        ]
      ],
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | string |  |
| `subscriptions[]` | array<string> |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `GET /partner_api/v1/webhooks` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

