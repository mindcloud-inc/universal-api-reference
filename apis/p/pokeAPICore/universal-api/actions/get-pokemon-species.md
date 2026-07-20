# PokeAPI Core: Get Pokemon Species

Retrieves a Pokemon species from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon-species?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon-species?${params}`, {
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
| `idOrName` | string | yes | Pokemon species numeric ID or exact PokeAPI species name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_happiness": 1,
      "capture_rate": 1,
      "evolution_chain": {},
      "gender_rate": 1,
      "generation": {},
      "id": 1,
      "is_baby": true,
      "is_legendary": true,
      "is_mythical": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_happiness` | number | Base happiness value. |
| `capture_rate` | number | Species capture rate. |
| `evolution_chain` | object | Evolution chain reference. |
| `gender_rate` | number | Gender rate value from PokeAPI. |
| `generation` | object | Generation reference. |
| `id` | number | Numeric Pokemon species identifier. |
| `is_baby` | boolean | Whether the species is a baby Pokemon. |
| `is_legendary` | boolean | Whether the species is legendary. |
| `is_mythical` | boolean | Whether the species is mythical. |
| `name` | string | Species resource name. |
| `names` | array<object> | Localized names. |
| `order` | number | Species ordering value. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /pokemon-species/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-species.md) for the provider-specific parameters and requirements.

