# Codeberg: List Notifications



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-notifications?${params}`, {
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
      "id": 1,
      "pinned": true,
      "subject": {
        "html_url": "https://example.com",
        "state": "string",
        "title": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "unread": true,
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
| `id` | number |  |
| `pinned` | boolean |  |
| `subject.html_url` | string |  |
| `subject.state` | string |  |
| `subject.title` | string |  |
| `subject.type` | string |  |
| `subject.url` | string |  |
| `unread` | boolean |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /notifications` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.

