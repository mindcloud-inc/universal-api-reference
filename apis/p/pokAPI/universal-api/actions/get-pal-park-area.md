# PokéAPI: Get Pal Park Area

Retrieves details for a pal park area from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pal-park-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pal-park-area?connectionId=$CONNECTION_ID&palParkAreaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "palParkAreaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pal-park-area?${params}`, {
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
| `palParkAreaId` | string | yes | Identifier for the requested Pal Park Area record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_encounters": [
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
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon_encounters` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pal-park-area/:palParkAreaId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pal-park-area.md) for the provider-specific parameters and requirements.

