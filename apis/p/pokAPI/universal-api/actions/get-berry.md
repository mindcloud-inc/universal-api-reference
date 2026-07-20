# PokéAPI: Get Berry

Retrieves details for a berry from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry?connectionId=$CONNECTION_ID&berryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "berryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry?${params}`, {
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
| `berryId` | string | yes | Identifier for the requested Berry record. |

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
| `firmness` | object |  |
| `flavors` | array<object> |  |
| `growth_time` | number |  |
| `id` | number |  |
| `item` | object |  |
| `max_harvest` | number |  |
| `name` | string |  |
| `natural_gift_power` | number |  |
| `natural_gift_type` | object |  |
| `size` | number |  |
| `smoothness` | number |  |
| `soil_dryness` | number |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET berry/:berryId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-berry.md) for the provider-specific parameters and requirements.

