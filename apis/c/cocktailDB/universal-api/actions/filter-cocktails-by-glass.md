# CocktailDB: Filter Cocktails by Glass



```
GET https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-glass
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CocktailDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-glass?connectionId=$CONNECTION_ID&glass=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "glass": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cocktailDB/latest/actions/filter-cocktails-by-glass?${params}`, {
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
| `glass` | string | yes | Filter cocktails by glass type. |

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

Through the native CocktailDB API, this operation is `GET /filter.php` (base URL `https://www.thecocktaildb.com/api/json/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-cocktails-by-glass.md) for the provider-specific parameters and requirements.

