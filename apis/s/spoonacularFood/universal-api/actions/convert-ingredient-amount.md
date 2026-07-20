# Spoonacular Food: Convert Ingredient Amount

Converts ingredient amounts in Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/convert-ingredient-amount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/convert-ingredient-amount?connectionId=$CONNECTION_ID&ingredientName=Ava%20Chen&sourceAmount=1&sourceUnit=string&targetUnit=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredientName": "Ava Chen",
  "sourceAmount": "1",
  "sourceUnit": "string",
  "targetUnit": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/convert-ingredient-amount?${params}`, {
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
| `ingredientName` | string | yes | Ingredient to convert. |
| `sourceAmount` | number | yes | Amount to convert from. |
| `sourceUnit` | string | yes | Unit to convert from. |
| `targetUnit` | string | yes | Unit to convert to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "sourceAmount": 1,
      "sourceUnit": "string",
      "targetAmount": 1,
      "targetUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `sourceAmount` | number |  |
| `sourceUnit` | string |  |
| `targetAmount` | number |  |
| `targetUnit` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /recipes/convert` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-ingredient-amount.md) for the provider-specific parameters and requirements.

