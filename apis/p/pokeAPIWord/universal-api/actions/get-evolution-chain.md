# PokeAPI Word: Get Evolution Chain

Retrieves evolution chain details from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-chain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-chain?connectionId=$CONNECTION_ID&evolutionChainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evolutionChainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-chain?${params}`, {
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
| `evolutionChainId` | string | yes | Identifier for the requested evolution chain. Use an ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baby_trigger_item": {},
      "chain": {},
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baby_trigger_item` | object |  |
| `chain` | object |  |
| `id` | number |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET evolution-chain/[:evolutionChainId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evolution-chain.md) for the provider-specific parameters and requirements.

