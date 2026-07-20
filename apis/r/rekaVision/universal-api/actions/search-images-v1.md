# Reka Vision: Search Images (V1)

Finds images in Reka Vision by text query.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/search-images-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/search-images-v1?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/search-images-v1?${params}`, {
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
| `query` | string | yes |  |
| `maxResults` | number | no |  |
| `searchMode` | list<string> | no | One of: `joined`, `vision`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageWeight` | number | no |  |
| `textWeight` | number | no |  |
| `threshold` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageId": "string",
      "imageMetadata": {},
      "imageUrl": "https://example.com",
      "score": 1,
      "uploadTimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageId` | string |  |
| `imageMetadata` | object |  |
| `imageUrl` | string |  |
| `score` | number |  |
| `uploadTimestamp` | number |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/images/search` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-images-v1.md) for the provider-specific parameters and requirements.

