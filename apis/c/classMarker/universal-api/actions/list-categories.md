# ClassMarker: List Categories



```
GET https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "parentCategories": [
          {
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
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.parentCategories[].categories[].categoryId` | number |  |
| `data.parentCategories[].categories[].categoryName` | string |  |
| `data.parentCategories[].categories[].parentCategoryId` | number |  |
| `data.parentCategories[].parentCategoryId` | number |  |
| `data.parentCategories[].parentCategoryName` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `GET /v1/categories.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

