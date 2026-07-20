# Instapaper: Delete Bookmark



```
DELETE https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/delete-bookmark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/delete-bookmark?connectionId=$CONNECTION_ID&bookmarkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookmarkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/delete-bookmark?${params}`, {
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
| `bookmarkId` | string | yes | The bookmark to permanently delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmarkId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmarkId` | string | Bookmark ID returned through primary-key fallback when delete succeeds with an empty response body. |

## Native endpoint

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/delete` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bookmark.md) for the provider-specific parameters and requirements.

