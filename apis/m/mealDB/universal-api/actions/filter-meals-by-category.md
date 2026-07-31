# MealDB: Filter Meals by Category



```
GET https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MealDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-category?${params}`, {
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
| `category` | string | yes | Meal category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meals": [
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
| `meals` | array<object> | Native MealDB meals envelope. Filter items preserve idMeal, strMeal, strMealThumb, strArea, and strCountry fields. |

## Native endpoint

Through the native MealDB API, this operation is `GET /filter.php` (base URL `https://www.themealdb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-meals-by-category.md) for the provider-specific parameters and requirements.

