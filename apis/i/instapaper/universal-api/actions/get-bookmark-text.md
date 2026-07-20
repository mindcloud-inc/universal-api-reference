# Instapaper: Get Bookmark Text



```
GET https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/get-bookmark-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instapaper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/get-bookmark-text?connectionId=$CONNECTION_ID&bookmarkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookmarkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/get-bookmark-text?${params}`, {
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
| `bookmarkId` | string | yes | The bookmark whose text view you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Processed bookmark text-view HTML returned by Instapaper. |

## Native endpoint

Through the native Instapaper API, this operation is `POST /api/1/bookmarks/get_text` (base URL `https://www.instapaper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bookmark-text.md) for the provider-specific parameters and requirements.

