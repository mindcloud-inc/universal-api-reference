# Dappier: Get Cat Care Recommendations

Retrieves cat care article recommendations from Dappier.

```
GET https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-cat-care-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dappier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-cat-care-recommendations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dappier/latest/actions/get-cat-care-recommendations?${params}`, {
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
      "author": "string",
      "imageUrl": "https://example.com",
      "previewContent": "string",
      "pubdate": "string",
      "pubdateUnix": 1,
      "score": 1,
      "site": "string",
      "siteDomain": "string",
      "sourceUrl": "https://example.com",
      "summary": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `imageUrl` | string |  |
| `previewContent` | string |  |
| `pubdate` | string |  |
| `pubdateUnix` | number |  |
| `score` | number |  |
| `site` | string |  |
| `siteDomain` | string |  |
| `sourceUrl` | string |  |
| `summary` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Dappier API, this operation is `POST /app/v2/search` (base URL `https://api.dappier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cat-care-recommendations.md) for the provider-specific parameters and requirements.

