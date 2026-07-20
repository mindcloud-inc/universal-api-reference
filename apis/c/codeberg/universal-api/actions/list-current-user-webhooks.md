# Codeberg: List Current User Webhooks



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-webhooks?${params}`, {
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
      "active": true,
      "authorization_header": "string",
      "branch_filter": "string",
      "content_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `authorization_header` | string |  |
| `branch_filter` | string |  |
| `content_type` | string |  |
| `created_at` | date |  |
| `events` | array<string> |  |
| `id` | number |  |
| `type` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/hooks` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-webhooks.md) for the provider-specific parameters and requirements.

