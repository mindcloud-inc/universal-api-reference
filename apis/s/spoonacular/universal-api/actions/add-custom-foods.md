# Spoonacular: Add Custom Foods

Creates a custom food in Spoonacular.

```
POST https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/add-custom-foods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/add-custom-foods" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hash": "string",
  "requestBody": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/add-custom-foods', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hash": "string",
    "requestBody": "string",
    "username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hash` | string | yes | Required by the Spoonacular endpoint. |
| `requestBody` | string | yes | The required request body. |
| `username` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Spoonacular API, this operation is `POST /food/customFoods/add` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-foods.md) for the provider-specific parameters and requirements.

