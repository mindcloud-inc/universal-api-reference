# Codemagic: List User Notifications

Retrieves notifications for the authenticated Codemagic user.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-user-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-user-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-user-notifications?${params}`, {
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
      "body_text": "string",
      "category": "string",
      "cta_text": "string",
      "cta_url": "https://example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body_text` | string |  |
| `category` | string |  |
| `cta_text` | string |  |
| `cta_url` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/user/notifications` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-notifications.md) for the provider-specific parameters and requirements.

