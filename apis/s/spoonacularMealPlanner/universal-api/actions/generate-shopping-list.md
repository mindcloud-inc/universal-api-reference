# Spoonacular Meal Planner: Generate Shopping List

Creates a shopping list from a meal plan in Spoonacular Meal Planner.

```
POST https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-shopping-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-shopping-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/generate-shopping-list', {
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
| `endDate` | string | no | Shopping-list end date in yyyy-mm-dd format. |
| `hash` | string | no | Private hash returned by Connect User. |
| `startDate` | string | no | Shopping-list start date in yyyy-mm-dd format. |
| `username` | string | no | Spoonacular username returned by Connect User. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aisles": [
        {}
      ],
      "cost": 1,
      "endDate": 1,
      "startDate": 1
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
| `endDate` | number |  |
| `startDate` | number |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `POST /mealplanner/{username}/shopping-list/{start-date}/{end-date}` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-shopping-list.md) for the provider-specific parameters and requirements.

