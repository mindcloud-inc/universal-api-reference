# Document360: List Article Versions



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-article-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-article-versions?connectionId=$CONNECTION_ID&articleId=string&langCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "string",
  "langCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-article-versions?${params}`, {
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
| `articleId` | string | yes | The ID of the article |
| `langCode` | string | yes | The language code of the article |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseVersion": 1,
      "createdAt": "string",
      "createdBy": "string",
      "modifiedAt": "string",
      "profileUrl": "https://example.com",
      "status": 1,
      "versionNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseVersion` | number |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `modifiedAt` | string |  |
| `profileUrl` | string |  |
| `status` | number |  |
| `versionNumber` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Articles/:articleId/:langCode/versions` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-article-versions.md) for the provider-specific parameters and requirements.

