# Instapaper: List Bookmark Highlights



```
GET https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmark-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmark-highlights?connectionId=$CONNECTION_ID&bookmarkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookmarkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/list-bookmark-highlights?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookmarkId` | string | yes | The bookmark whose highlights you want to list. |

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

Through the native Instapaper API, this operation is `POST /api/1.1/bookmarks/:bookmarkId/highlights` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookmark-highlights.md) for the provider-specific parameters and requirements.

