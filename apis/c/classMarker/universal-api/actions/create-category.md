# ClassMarker: Create Category



```
POST https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryName": "Ava Chen",
  "parentCategoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryName": "Ava Chen",
    "parentCategoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryName` | string | yes | Name of the category to create. |
| `parentCategoryId` | number | yes | Numeric ClassMarker parent category ID that will own the category. |
| `verifyOnly` | boolean | no | Validate the request without creating the category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "category": {
          "categoryId": 1,
          "categoryName": "Ava Chen",
          "parentCategoryId": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.category.categoryId` | number |  |
| `data.category.categoryName` | string |  |
| `data.category.parentCategoryId` | number |  |

## Native endpoint

Through the native ClassMarker API, this operation is `POST /v1/categories/category.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

