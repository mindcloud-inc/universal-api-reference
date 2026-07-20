# PokeAPI Core: Get Berry

Retrieves a berry from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-berry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-berry?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-berry?${params}`, {
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
| `idOrName` | string | yes | Berry numeric ID or exact PokeAPI berry name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firmness": {},
      "flavors": [
        {}
      ],
      "growth_time": 1,
      "id": 1,
      "item": {},
      "max_harvest": 1,
      "name": "Ava Chen",
      "natural_gift_power": 1,
      "natural_gift_type": {},
      "size": 1,
      "smoothness": 1,
      "soil_dryness": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firmness` | object | Berry firmness reference. |
| `flavors` | array<object> | Berry flavor potency records. |
| `growth_time` | number | Growth time in hours. |
| `id` | number | Numeric berry identifier. |
| `item` | object | Related item reference. |
| `max_harvest` | number | Maximum harvest count. |
| `name` | string | Berry resource name. |
| `natural_gift_power` | number | Natural gift power value. |
| `natural_gift_type` | object | Natural gift type reference. |
| `size` | number | Berry size value. |
| `smoothness` | number | Berry smoothness value. |
| `soil_dryness` | number | Soil dryness value. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /berry/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-berry.md) for the provider-specific parameters and requirements.

