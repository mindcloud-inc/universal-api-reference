# PokéAPI: Get Encounter Condition Value

Retrieves details for an encounter condition value from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-encounter-condition-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-encounter-condition-value?connectionId=$CONNECTION_ID&encounterConditionValueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "encounterConditionValueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-encounter-condition-value?${params}`, {
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
| `encounterConditionValueId` | string | yes | Identifier for the requested Encounter Condition Value record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "condition": {},
      "id": 1,
      "name": "Ava Chen",
      "names": [
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
| `condition` | object |  |
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET encounter-condition-value/:encounterConditionValueId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-encounter-condition-value.md) for the provider-specific parameters and requirements.

