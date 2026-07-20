# Spoonacular Meal Planner: Add to Meal Plan

Creates a meal plan item in Spoonacular Meal Planner.

```
POST https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-to-meal-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-to-meal-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/add-to-meal-plan', {
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
| `date` | string | no | Meal plan date in yyyy-mm-dd format. |
| `hash` | string | no | Private hash returned by Connect User. |
| `position` | string | no | Position in the meal slot. |
| `slot` | string | no | Meal slot: 1 breakfast, 2 lunch, or 3 dinner. |
| `type` | string | no | Meal plan item type, such as RECIPE, PRODUCT, MENU_ITEM, CUSTOM_FOOD, or INGREDIENTS. |
| `username` | string | no | Spoonacular username returned by Connect User. |
| `value` | string | no | Meal plan item value object for the selected type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
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
| `status` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `POST /mealplanner/{username}/items` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-to-meal-plan.md) for the provider-specific parameters and requirements.

