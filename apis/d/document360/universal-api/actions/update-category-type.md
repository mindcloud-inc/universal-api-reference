# Document360: Update Category Type



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": "string",
  "categoryType": 1,
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/update-category-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": "string",
    "categoryType": 1,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryId` | string | yes | The ID of the category |
| `categoryType` | number | yes | 0 Folder, 1 Page, 2 Index |
| `userId` | string | yes | The ID of the team account |

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
| `warnings` | array<object> |  |

## Native endpoint

Through the native Document360 API, this operation is `PUT /v2/Categories/:categoryId/updateCategoryType` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category-type.md) for the provider-specific parameters and requirements.

