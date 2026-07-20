# Instructure: Update Bookmark

Updates an existing bookmark in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookmarkId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-bookmark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookmarkId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookmarkId` | string | yes | The Canvas bookmark ID. |
| `data` | string | no | Associated bookmark data. |
| `name` | string | no | The name of the bookmark. |
| `position` | string | no | The position of the bookmark. |
| `url` | string | no | The URL of the bookmark. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `id` | number |  |
| `name` | string |  |
| `position` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /users/self/bookmarks/:bookmark_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bookmark.md) for the provider-specific parameters and requirements.

