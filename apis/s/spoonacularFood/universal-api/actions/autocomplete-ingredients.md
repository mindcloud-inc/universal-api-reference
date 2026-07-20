# Spoonacular Food: Autocomplete Ingredients

Finds ingredient suggestions in Spoonacular Food by partial name.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-ingredients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-ingredients?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/autocomplete-ingredients?${params}`, {
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
| `query` | string | yes | Partial or full ingredient name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `image` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/ingredients/autocomplete` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-ingredients.md) for the provider-specific parameters and requirements.

