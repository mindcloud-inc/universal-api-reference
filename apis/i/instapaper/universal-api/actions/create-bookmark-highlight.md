# Instapaper: Create Bookmark Highlight



```
POST https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/create-bookmark-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/create-bookmark-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookmarkId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/create-bookmark-highlight', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookmarkId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookmarkId` | string | yes | The bookmark where the highlight will be created. |
| `position` | string | no | Optional 0-indexed position of the text in the content. |
| `text` | string | yes | The highlight text. HTML tags should be unescaped. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmarkId": 1,
      "highlightId": 1,
      "position": 1,
      "text": "string",
      "time": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmarkId` | number |  |
| `highlightId` | number |  |
| `position` | number |  |
| `text` | string |  |
| `time` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Instapaper API, this operation is `POST /api/1.1/bookmarks/:bookmarkId/highlight` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bookmark-highlight.md) for the provider-specific parameters and requirements.

