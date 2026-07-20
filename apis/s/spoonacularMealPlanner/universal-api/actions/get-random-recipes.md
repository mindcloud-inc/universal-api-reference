# Spoonacular Meal Planner: Get Random Recipes

Retrieves random recipes from Spoonacular Meal Planner.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-random-recipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-random-recipes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-random-recipes?${params}`, {
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
| `tags` | string | no | Comma-separated tags to narrow random recipes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recipes": [
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
| `recipes` | array<object> |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/random` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-recipes.md) for the provider-specific parameters and requirements.

