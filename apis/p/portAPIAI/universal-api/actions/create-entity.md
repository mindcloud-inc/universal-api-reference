# Port API AI: Create Entity

Creates an entity in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprintIdentifier": "string",
  "identifier": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprintIdentifier": "string",
    "identifier": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprintIdentifier` | string | yes | The Port blueprint identifier. |
| `identifier` | string | yes | Entity identifier |
| `title` | string | yes | Entity title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints/:blueprint_identifier/entities` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entity.md) for the provider-specific parameters and requirements.

