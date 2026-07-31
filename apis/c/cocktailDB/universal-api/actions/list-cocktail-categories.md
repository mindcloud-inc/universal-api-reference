# CocktailDB: List Cocktail Categories



```
GET https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/list-cocktail-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CocktailDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/list-cocktail-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/list-cocktail-categories?${params}`, {
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
      "drinks": [
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
| `drinks` | array<object> | Provider response collection of drinks or documented drink-list values. |

## Native endpoint

Through the native CocktailDB API, this operation is `GET /list.php?c=list` (base URL `https://www.thecocktaildb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cocktail-categories.md) for the provider-specific parameters and requirements.

