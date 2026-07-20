# PokéAPI: Get Pokemon Encounters

Retrieves pokemon encounter locations from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-encounters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-encounters?connectionId=$CONNECTION_ID&pokemonId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-encounters?${params}`, {
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
| `pokemonId` | string | yes | The Pokemon identifier or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location_area": {},
      "version_details": [
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
| `location_area` | object |  |
| `version_details` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokemon/:pokemonId/encounters` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-encounters.md) for the provider-specific parameters and requirements.

