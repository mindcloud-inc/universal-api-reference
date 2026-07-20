# PokeAPI Word Universal API Examples

These examples use the MindCloud API key and PokeAPI Word connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Ability

Retrieves details for an ability from PokeAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-ability?connectionId=$CONNECTION_ID&abilityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "abilityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-ability?${params}`, {
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
      "generation": {},
      "id": 1,
      "is_main_series": true,
      "name": "Ava Chen",
      "pokemon": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Ability action reference](actions/get-ability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pokeAPIWord/latest/actions/get-ability).
