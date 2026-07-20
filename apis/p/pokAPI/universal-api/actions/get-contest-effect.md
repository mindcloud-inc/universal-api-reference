# PokéAPI: Get Contest Effect

Retrieves details for a contest effect from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-contest-effect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-contest-effect?connectionId=$CONNECTION_ID&contestEffectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contestEffectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-contest-effect?${params}`, {
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
| `contestEffectId` | string | yes | Identifier for the requested Contest Effect record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appeal": 1,
      "effect_entries": [
        {}
      ],
      "flavor_text_entries": [
        {}
      ],
      "id": 1,
      "jam": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appeal` | number |  |
| `effect_entries` | array<object> |  |
| `flavor_text_entries` | array<object> |  |
| `id` | number |  |
| `jam` | number |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET contest-effect/:contestEffectId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contest-effect.md) for the provider-specific parameters and requirements.

