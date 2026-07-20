# You.com: Search Images

Retrieves image search results from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search-images?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/search-images?${params}`, {
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
| `query` | string | yes | Image search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": {
        "results": [
          [
            {}
          ]
        ]
      },
      "metadata": {
        "query": "string",
        "searchUuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images` | object | Top-level image search response. |
| `images.results[]` | array<object> | Image search result items. |
| `images.results[].imageUrl` | string | Direct image URL. |
| `images.results[].pageUrl` | string | Source page URL for the image result. |
| `images.results[].title` | string | Image result title. |
| `metadata` | object | Image search metadata. |
| `metadata.query` | string | Echoed image search query. |
| `metadata.searchUuid` | string | Search request identifier. |

## Native endpoint

Through the native You.com API, this operation is `GET https://image-search.ydc-index.io/images` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-images.md) for the provider-specific parameters and requirements.

