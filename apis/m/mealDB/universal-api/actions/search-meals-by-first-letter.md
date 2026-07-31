# MealDB: Search Meals by First Letter



```
GET https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/search-meals-by-first-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MealDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/search-meals-by-first-letter?connectionId=$CONNECTION_ID&firstLetter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstLetter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/search-meals-by-first-letter?${params}`, {
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
| `firstLetter` | string | yes | Single letter used to search meal names. |

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
| `meals` | array<object> | Native MealDB meals envelope. Each meal preserves idMeal, recipe metadata, strMealThumb, and strIngredient1 through strIngredient20 with matching strMeasure1 through strMeasure20 slots; no ingredient-array normalization is applied. |

## Native endpoint

Through the native MealDB API, this operation is `GET /search.php` (base URL `https://www.themealdb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-meals-by-first-letter.md) for the provider-specific parameters and requirements.

