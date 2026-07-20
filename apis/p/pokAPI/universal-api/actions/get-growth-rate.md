# PokéAPI: Get Growth Rate

Retrieves details for a growth rate from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-growth-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-growth-rate?connectionId=$CONNECTION_ID&growthRateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "growthRateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-growth-rate?${params}`, {
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
| `growthRateId` | string | yes | Identifier for the requested Growth Rate record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "descriptions": [
        {}
      ],
      "formula": "string",
      "id": 1,
      "levels": [
        {}
      ],
      "name": "Ava Chen",
      "pokemon_species": [
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
| `descriptions` | array<object> |  |
| `formula` | string |  |
| `id` | number |  |
| `levels` | array<object> |  |
| `name` | string |  |
| `pokemon_species` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET growth-rate/:growthRateId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-growth-rate.md) for the provider-specific parameters and requirements.

