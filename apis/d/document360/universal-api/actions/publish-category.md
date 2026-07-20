# Document360: Publish Category



```
PUT https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryId": "string",
  "langCode": "string",
  "userId": "string",
  "versionNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/publish-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryId": "string",
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
| `categoryId` | string | yes | The ID of the category |
| `langCode` | string | yes | Language code of the category |
| `userId` | string | yes | Team account ID responsible for the publish |
| `versionNumber` | number | yes | Category version number to publish |
| `publishMessage` | string | no | Optional publish message |

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

Through the native Document360 API, this operation is `POST /v2/Categories/:categoryId/:langCode/publish` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-category.md) for the provider-specific parameters and requirements.

