# PokeAPI Core: List Pokemon Species

Retrieves a page of Pokemon species from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/list-pokemon-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/list-pokemon-species?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/list-pokemon-species?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number | Total number of Pokemon species resources available. |
| `next` | string | URL for the next page of results, when available. |
| `previous` | string | URL for the previous page of results, when available. |
| `results` | array<object> | Pokemon species resource references for the current page. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /pokemon-species/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pokemon-species.md) for the provider-specific parameters and requirements.

