# Document360: Create Category



```
POST https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectVersionId": "string",
  "categoryType": 1,
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectVersionId": "string",
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
| `name` | string | yes | The name of the category |
| `projectVersionId` | string | yes | Project version where the category will be created |
| `order` | number | no | The position inside the parent category |
| `parentCategoryId` | string | no | Parent category for nesting |
| `content` | string | no | Category content for page or index categories |
| `categoryType` | number | yes | 0 Folder, 1 Page, 2 Index |
| `userId` | string | yes | Team account ID creating the category |
| `contentType` | number | no | 0 Markdown, 1 WYSIWYG, 2 Advanced WYSIWYG |
| `slug` | string | no | Optional URL-friendly slug |

## Response

```json
{
  "success": true,
  "data": [
    {
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `order` | number |  |

## Native endpoint

Through the native Document360 API, this operation is `POST /v2/Categories` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

