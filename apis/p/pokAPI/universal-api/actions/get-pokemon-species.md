# PokéAPI: Get Pokemon Species

Retrieves details for a pokemon species from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-species?connectionId=$CONNECTION_ID&pokemonSpeciesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonSpeciesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-species?${params}`, {
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
| `pokemonSpeciesId` | string | yes | Identifier for the requested Pokemon Species record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_happiness": 1,
      "capture_rate": 1,
      "color": {},
      "egg_groups": [
        {}
      ],
      "evolution_chain": {},
      "evolves_from_species": "string",
      "flavor_text_entries": [
        {}
      ],
      "form_descriptions": [
        {}
      ],
      "forms_switchable": true,
      "gender_rate": 1,
      "genera": [
        {}
      ],
      "generation": {},
      "growth_rate": {},
      "habitat": {},
      "has_gender_differences": true,
      "hatch_counter": 1,
      "id": 1,
      "is_baby": true,
      "is_legendary": true,
      "is_mythical": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "order": 1,
      "pal_park_encounters": [
        {}
      ],
      "pokedex_numbers": [
        {}
      ],
      "shape": {},
      "varieties": [
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
| `base_happiness` | number |  |
| `capture_rate` | number |  |
| `color` | object |  |
| `egg_groups` | array<object> |  |
| `evolution_chain` | object |  |
| `evolves_from_species` | string |  |
| `flavor_text_entries` | array<object> |  |
| `form_descriptions` | array<object> |  |
| `forms_switchable` | boolean |  |
| `gender_rate` | number |  |
| `genera` | array<object> |  |
| `generation` | object |  |
| `growth_rate` | object |  |
| `habitat` | object |  |
| `has_gender_differences` | boolean |  |
| `hatch_counter` | number |  |
| `id` | number |  |
| `is_baby` | boolean |  |
| `is_legendary` | boolean |  |
| `is_mythical` | boolean |  |
| `name` | string |  |
| `names` | array<object> |  |
| `order` | number |  |
| `pal_park_encounters` | array<object> |  |
| `pokedex_numbers` | array<object> |  |
| `shape` | object |  |
| `varieties` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokemon-species/:pokemonSpeciesId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-species.md) for the provider-specific parameters and requirements.

