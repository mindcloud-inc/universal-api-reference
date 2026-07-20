# Spoonacular Meal Planner: Compute Shopping List

Computes a shopping list from food strings in Spoonacular Meal Planner.

```
POST https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/compute-shopping-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/compute-shopping-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/compute-shopping-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<string> | yes | Array of simple food strings to compute into a shopping list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aisles": [
        {}
      ],
      "cost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aisles` | array<object> |  |
| `cost` | number |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `POST /mealplanner/shopping-list/compute` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compute-shopping-list.md) for the provider-specific parameters and requirements.

