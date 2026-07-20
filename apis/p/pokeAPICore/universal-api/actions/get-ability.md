# PokeAPI Core: Get Ability

Retrieves an ability from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-ability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOrName` | string | yes | Ability numeric ID or exact PokeAPI ability name. Example: `1`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effect_entries` | array<object> | Localized effect text entries. |
| `flavor_text_entries` | array<object> | Localized flavor text entries. |
| `generation` | object | Generation reference. |
| `id` | number | Numeric ability identifier. |
| `is_main_series` | boolean | Whether the ability is part of the main series games. |
| `name` | string | Ability resource name. |
| `names` | array<object> | Localized ability names. |
| `pokemon` | array<object> | Pokemon that can have this ability. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /ability/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ability.md) for the provider-specific parameters and requirements.

