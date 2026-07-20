# Spoonacular Meal Planner: Get Meal Plan Template

Retrieves a meal plan template from Spoonacular Meal Planner.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-meal-plan-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-meal-plan-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/get-meal-plan-template?${params}`, {
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
| `hash` | string | no | Private hash returned by Connect User. |
| `id` | string | no | Meal plan template ID. |
| `username` | string | no | Spoonacular username returned by Connect User. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "days": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days` | array<object> |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `GET /mealplanner/{username}/templates/{id}` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meal-plan-template.md) for the provider-specific parameters and requirements.

