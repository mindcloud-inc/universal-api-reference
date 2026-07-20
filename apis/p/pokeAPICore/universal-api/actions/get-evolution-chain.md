# PokeAPI Core: Get Evolution Chain

Retrieves an evolution chain from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-evolution-chain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-evolution-chain?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-evolution-chain?${params}`, {
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
| `id` | string | yes | Evolution chain numeric ID. Example: `1`. |

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
| `baby_trigger_item` | object | Baby trigger item reference, when available. |
| `chain` | object | Nested evolution chain starting point and evolution details. |
| `id` | number | Numeric evolution chain identifier. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /evolution-chain/[:id]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evolution-chain.md) for the provider-specific parameters and requirements.

