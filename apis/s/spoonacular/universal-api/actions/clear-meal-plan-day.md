# Spoonacular: Clear Meal Plan Day

Clears a day from a Spoonacular meal plan.

```
DELETE https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/clear-meal-plan-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/clear-meal-plan-day?connectionId=$CONNECTION_ID&date=string&hash=string&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "hash": "string",
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/clear-meal-plan-day?${params}`, {
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
| `date` | string | yes | Required by the Spoonacular endpoint. |
| `hash` | string | yes | Required by the Spoonacular endpoint. |
| `username` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Spoonacular API, this operation is `DELETE /mealplanner/{username}/day/{date}` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-meal-plan-day.md) for the provider-specific parameters and requirements.

