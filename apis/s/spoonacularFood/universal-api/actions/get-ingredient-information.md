# Spoonacular Food: Get Ingredient Information

Retrieves ingredient information from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-information?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-information?${params}`, {
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
| `id` | number | yes | The Spoonacular ingredient ID. |
| `amount` | number | no | Amount of the ingredient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "id": 1,
      "image": "string",
      "name": "Ava Chen",
      "nutrition": {},
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `id` | number |  |
| `image` | string |  |
| `name` | string |  |
| `nutrition` | object |  |
| `unit` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/ingredients/:id/information` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ingredient-information.md) for the provider-specific parameters and requirements.

