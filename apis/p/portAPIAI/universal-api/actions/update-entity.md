# Port API AI: Update Entity

Updates an entity in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprintIdentifier": "string",
  "entityIdentifier": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-entity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprintIdentifier": "string",
    "entityIdentifier": "string",
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
| `entityIdentifier` | string | yes | The Port entity identifier. |
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

Through the native Port API AI API, this operation is `PATCH /blueprints/:blueprint_identifier/entities/:entity_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-entity.md) for the provider-specific parameters and requirements.

