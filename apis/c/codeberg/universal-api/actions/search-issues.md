# Codeberg: Search Issues



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-issues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-issues?${params}`, {
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
      "assets": [
        {
          "name": "Ava Chen"
        }
      ],
      "body": "string",
      "closed_at": "2026-05-07T12:00:00.000Z",
      "comments": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "due_date": "2026-05-07T12:00:00.000Z",
      "html_url": "https://example.com",
      "id": 1,
      "is_locked": true,
      "number": 1,
      "original_author": "string",
      "original_author_id": 1,
      "pin_order": 1,
      "ref": "string",
      "state": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": {
        "login": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assets[].name` | string |  |
| `body` | string |  |
| `closed_at` | date |  |
| `comments` | number |  |
| `created_at` | date |  |
| `due_date` | date |  |
| `html_url` | string |  |
| `id` | number |  |
| `is_locked` | boolean |  |
| `number` | number |  |
| `original_author` | string |  |
| `original_author_id` | number |  |
| `pin_order` | number |  |
| `ref` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user.login` | string |  |
| `user.username` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /repos/issues/search` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-issues.md) for the provider-specific parameters and requirements.

