# Instapaper: Add Bookmark



```
POST https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/add-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/add-bookmark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/add-bookmark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | string | no | Optional 1 or 0 value that archives the bookmark while adding it. |
| `content` | string | no | Optional full HTML content used when Instapaper cannot crawl the page itself. |
| `description` | string | no | Optional plaintext description or summary of the article. |
| `folderId` | string | no | Optional destination folder ID from List Folders. |
| `isPrivateFromSource` | string | no | Optional short label that makes the bookmark private and requires content. |
| `resolveFinalUrl` | string | no | Optional 1 or 0 value that tells Instapaper whether to resolve redirects before saving. |
| `tags` | string | no | Optional JSON array of tag objects, for example [{"name":"Tag Name"}]. |
| `title` | string | no | Optional title. If omitted, Instapaper tries to detect it. |
| `url` | string | no | The URL to save, unless you are creating a private bookmark. |

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

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/add` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-bookmark.md) for the provider-specific parameters and requirements.

