# Spoonacular Food: Get Analyzed Recipe Instructions

Retrieves analyzed recipe instructions from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-analyzed-recipe-instructions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-analyzed-recipe-instructions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-analyzed-recipe-instructions?${params}`, {
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
| `id` | number | yes | The Spoonacular recipe ID. |
| `stepBreakdown` | boolean | no | Whether to break down the recipe steps further. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "steps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `steps` | array<object> |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /recipes/:id/analyzedInstructions` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analyzed-recipe-instructions.md) for the provider-specific parameters and requirements.

