# Instapaper: Update Bookmark Read Progress



```
PUT https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/update-bookmark-read-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/update-bookmark-read-progress" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookmarkId": "string",
  "progress": "string",
  "progressTimestamp": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/update-bookmark-read-progress', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookmarkId": "string",
    "progress": "string",
    "progressTimestamp": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookmarkId` | string | yes | The bookmark whose reading progress you want to update. |
| `progress` | string | yes | Reading progress between 0.0 and 1.0. |
| `progressTimestamp` | string | yes | Unix timestamp when the progress was recorded. |

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

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/update_read_progress` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bookmark-read-progress.md) for the provider-specific parameters and requirements.

