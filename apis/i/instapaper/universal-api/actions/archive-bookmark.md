# Instapaper: Archive Bookmark



```
PUT https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/archive-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/archive-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookmarkId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/archive-bookmark', {
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
| `bookmarkId` | string | yes | The bookmark to move to the archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmarkId": 1,
      "description": "string",
      "hash": "string",
      "progress": 1,
      "progressTimestamp": 1,
      "title": "string",
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
| `bookmarkId` | number |  |
| `description` | string |  |
| `hash` | string |  |
| `progress` | number |  |
| `progressTimestamp` | number |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/archive` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-bookmark.md) for the provider-specific parameters and requirements.

