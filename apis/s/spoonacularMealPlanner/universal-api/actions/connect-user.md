# Spoonacular Meal Planner: Connect User

Creates a connected user in Spoonacular Meal Planner.

```
POST https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/connect-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Meal Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/connect-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/connect-user', {
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
| `email` | string | no | User's email address. |
| `firstName` | string | no | User's first name. |
| `lastName` | string | no | User's last name. |
| `username` | string | no | Your app user's username for Spoonacular connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hash": "string",
      "spoonacularPassword": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hash` | string |  |
| `spoonacularPassword` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Spoonacular Meal Planner API, this operation is `POST /users/connect` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-user.md) for the provider-specific parameters and requirements.

