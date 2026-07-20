# Spoonacular Meal Planner: Autocomplete Recipe Search

Finds recipe suggestions in Spoonacular Meal Planner by title prefix.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/autocomplete-recipe-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/autocomplete-recipe-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/autocomplete-recipe-search?${params}`, {
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
| `query` | string | no | Recipe title prefix or search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "imageType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `imageType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /recipes/autocomplete` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-recipe-search.md) for the provider-specific parameters and requirements.

