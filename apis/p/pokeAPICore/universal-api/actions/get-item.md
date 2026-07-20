# PokeAPI Core: Get Item

Retrieves an item from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-item?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-item?${params}`, {
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
| `idOrName` | string | yes | Item numeric ID or exact PokeAPI item name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "category": {},
      "cost": 1,
      "effect_entries": [
        {}
      ],
      "fling_effect": {},
      "fling_power": 1,
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "sprites": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> | Item attribute references. |
| `category` | object | Item category reference. |
| `cost` | number | Item cost value. |
| `effect_entries` | array<object> | Localized effect entries. |
| `fling_effect` | object | Fling effect reference, when available. |
| `fling_power` | number | Fling power, when available. |
| `id` | number | Numeric item identifier. |
| `name` | string | Item resource name. |
| `names` | array<object> | Localized item names. |
| `sprites` | object | Item sprite URLs. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /item/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

