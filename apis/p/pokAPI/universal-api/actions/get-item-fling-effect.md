# PokéAPI: Get Item Fling Effect

Retrieves details for an item fling effect from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-fling-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-fling-effect?connectionId=$CONNECTION_ID&itemFlingEffectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemFlingEffectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-fling-effect?${params}`, {
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
| `itemFlingEffectId` | string | yes | Identifier for the requested Item Fling Effect record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "effect_entries": [
        {}
      ],
      "id": 1,
      "items": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effect_entries` | array<object> |  |
| `id` | number |  |
| `items` | array<object> |  |
| `name` | string |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET item-fling-effect/:itemFlingEffectId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-fling-effect.md) for the provider-specific parameters and requirements.

