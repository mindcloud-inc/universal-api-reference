# Spoonacular Recipe: Create Recipe Card

Generates a recipe card from a Spoonacular recipe.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/create-recipe-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/create-recipe-card?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/create-recipe-card?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/{id}/card` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipe-card.md) for the provider-specific parameters and requirements.

