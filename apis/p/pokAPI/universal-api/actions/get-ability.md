# PokéAPI: Get Ability

Retrieves details for an ability from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-ability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-ability?connectionId=$CONNECTION_ID&abilityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "abilityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-ability?${params}`, {
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
| `abilityId` | string | yes | Identifier for the requested Ability record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effect_changes": [
        {}
      ],
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
| `effect_changes` | array<object> |  |
| `effect_entries` | array<object> |  |
| `flavor_text_entries` | array<object> |  |
| `generation` | object |  |
| `id` | number |  |
| `is_main_series` | boolean |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET ability/:abilityId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ability.md) for the provider-specific parameters and requirements.

