# Spoonacular Meal Planner: Add Meal Plan Template

Creates a meal plan template in Spoonacular Meal Planner.

```
POST https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-meal-plan-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-meal-plan-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-meal-plan-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hash` | string | no | Private hash returned by Connect User. |
| `items` | string | no | Meal plan template items array. |
| `name` | string | no | Meal plan template name. |
| `publishAsPublic` | string | no | Whether to publish the template publicly. |
| `username` | string | no | Spoonacular username returned by Connect User. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `POST /mealplanner/{username}/templates` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-meal-plan-template.md) for the provider-specific parameters and requirements.

