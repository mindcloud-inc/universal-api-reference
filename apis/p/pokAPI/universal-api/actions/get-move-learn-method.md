# PokéAPI: Get Move Learn Method

Retrieves details for a move learn method from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-learn-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-learn-method?connectionId=$CONNECTION_ID&moveLearnMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moveLearnMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-learn-method?${params}`, {
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
| `moveLearnMethodId` | string | yes | Identifier for the requested Move Learn Method record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "descriptions": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "version_groups": [
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
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |
| `version_groups` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET move-learn-method/:moveLearnMethodId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move-learn-method.md) for the provider-specific parameters and requirements.

