# Port API AI: Create Multiple Entities

Creates multiple entities in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-multiple-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-multiple-entities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entities[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-multiple-entities', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entities[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprintIdentifier` | string | no | The Port blueprint identifier. |
| `entities[]` | array<object> | yes | Entities to create |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {}
      ],
      "errors": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities` | array<object> |  |
| `errors` | array<object> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints/:blueprint_identifier/entities/bulk` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-entities.md) for the provider-specific parameters and requirements.

