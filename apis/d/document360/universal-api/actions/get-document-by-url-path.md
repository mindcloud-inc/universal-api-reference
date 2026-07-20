# Document360: Get Document by URL Path



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-document-by-url-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-document-by-url-path?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/get-document-by-url-path?${params}`, {
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
| `url` | string | yes | The relative URL path |
| `applyRedirection` | boolean | no | Whether to apply active redirection rules |
| `isForDisplay` | boolean | no | Expand snippets and variables for display |
| `isPublished` | boolean | no | Whether to fetch the latest published version |
| `appendSASToken` | boolean | no | Whether to append SAS tokens for images and files |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article": {},
      "category": {},
      "documentType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | object |  |
| `category` | object |  |
| `documentType` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Project/Document` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-by-url-path.md) for the provider-specific parameters and requirements.

