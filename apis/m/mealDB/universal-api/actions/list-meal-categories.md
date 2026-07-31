# MealDB: List Meal Categories



```
GET https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/list-meal-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MealDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/list-meal-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/list-meal-categories?${params}`, {
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
      "categories": [
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
| `categories` | array<object> | Native MealDB categories envelope. Each category preserves idCategory, strCategory, strCategoryThumb, and strCategoryDescription. |

## Native endpoint

Through the native MealDB API, this operation is `GET /categories.php` (base URL `https://www.themealdb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meal-categories.md) for the provider-specific parameters and requirements.

