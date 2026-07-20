# Document360: Publish Article



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": "string",
  "langCode": "string",
  "userId": "string",
  "versionNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": "string",
    "langCode": "string",
    "userId": "string",
    "versionNumber": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | string | yes | The ID of the article |
| `langCode` | string | yes | The language code of the article |
| `userId` | string | yes | The team account publishing the article |
| `versionNumber` | number | yes | The version to publish |
| `publishMessage` | string | no | A short publish note |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "extensionData": {},
      "information": [
        {}
      ],
      "success": true,
      "url": "https://example.com",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `extensionData` | object |  |
| `information` | array<object> |  |
| `success` | boolean |  |
| `url` | string |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Document360 API, this operation is `POST /v2/Articles/:articleId/:langCode/publish` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-article.md) for the provider-specific parameters and requirements.

