# MealDB: Filter Meals by Area



```
GET https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MealDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area?connectionId=$CONNECTION_ID&area=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "area": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area?${params}`, {
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
| `area` | string | yes | Meal area. |

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

Through the native MealDB API, this operation is `GET /filter.php` (base URL `https://www.themealdb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-meals-by-area.md) for the provider-specific parameters and requirements.

