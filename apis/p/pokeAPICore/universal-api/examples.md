# PokeAPI Core Universal API Examples

These examples use the MindCloud API key and PokeAPI Core connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Ability

Retrieves an ability from PokeAPI Core.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-ability?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-ability?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "effect_entries": [
        {}
      ],
      "flavor_text_entries": [
        {}
      ],
      "generation": {},
      "id": 1,
      "is_main_series": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Ability action reference](actions/get-ability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pokeAPICore/latest/actions/get-ability).
