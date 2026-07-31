# CocktailDB: Search Ingredients by Name



```
GET https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/search-ingredients-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CocktailDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/search-ingredients-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/search-ingredients-by-name?${params}`, {
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
| `name` | string | yes | Search ingredients by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ingredients": [
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
| `ingredients` | array<object> | Provider response collection of ingredient records. |

## Native endpoint

Through the native CocktailDB API, this operation is `GET /search.php` (base URL `https://www.thecocktaildb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-ingredients-by-name.md) for the provider-specific parameters and requirements.

