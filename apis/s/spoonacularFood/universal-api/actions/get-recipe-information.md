# Spoonacular Food: Get Recipe Information

Retrieves recipe information from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-recipe-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-recipe-information?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-recipe-information?${params}`, {
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
| `includeNutrition` | boolean | no | Whether to include nutrition data in the recipe information. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "readyInMinutes": 1,
      "servings": 1,
      "sourceUrl": "https://example.com",
      "title": "string"
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
| `readyInMinutes` | number |  |
| `servings` | number |  |
| `sourceUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /recipes/:id/information` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipe-information.md) for the provider-specific parameters and requirements.

