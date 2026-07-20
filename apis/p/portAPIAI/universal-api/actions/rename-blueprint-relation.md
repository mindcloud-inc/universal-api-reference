# Port API AI: Rename Blueprint Relation

Updates a blueprint relation name in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/rename-blueprint-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/rename-blueprint-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprintIdentifier": "string",
  "relationIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/rename-blueprint-relation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprintIdentifier": "string",
    "relationIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprintIdentifier` | string | yes | The blueprint identifier. |
| `identifier` | string | no | New identifier for the relation. |
| `relationIdentifier` | string | yes | The relation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /blueprints/:blueprint_identifier/relations/:relation_identifier/rename` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-blueprint-relation.md) for the provider-specific parameters and requirements.

