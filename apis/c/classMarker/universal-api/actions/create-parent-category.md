# ClassMarker: Create Parent Category



```
POST https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-parent-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-parent-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentCategoryName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/create-parent-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentCategoryName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentCategoryName` | string | yes | Name of the parent category to create. |
| `verifyOnly` | boolean | no | Validate the request without creating the parent category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "parentCategory": {
          "categories": [
            {
              "categoryId": 1,
              "categoryName": "Ava Chen",
              "parentCategoryId": 1
            }
          ],
          "parentCategoryId": 1,
          "parentCategoryName": "Ava Chen"
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
| `data.parentCategory.categories[].categoryId` | number |  |
| `data.parentCategory.categories[].categoryName` | string |  |
| `data.parentCategory.categories[].parentCategoryId` | number |  |
| `data.parentCategory.parentCategoryId` | number |  |
| `data.parentCategory.parentCategoryName` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `POST /v1/categories/parent_category.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-parent-category.md) for the provider-specific parameters and requirements.

