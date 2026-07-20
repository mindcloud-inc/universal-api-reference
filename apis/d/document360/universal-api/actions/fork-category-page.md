# Document360: Fork Category Page



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/fork-category-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/fork-category-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": "string",
  "versionNumber": 1,
  "userId": "string",
  "langCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/fork-category-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": "string",
    "versionNumber": 1,
    "userId": "string",
    "langCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | yes | The ID of the category |
| `versionNumber` | number | yes | Category page version number to fork |
| `userId` | string | yes | Team account ID performing the fork |
| `langCode` | string | yes | Language code of the category page |

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

Through the native Document360 API, this operation is `PUT /v2/Categories/:categoryId/fork` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fork-category-page.md) for the provider-specific parameters and requirements.

