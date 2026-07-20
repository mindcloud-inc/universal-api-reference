# Port API AI: Delete Multiple Entities

Deletes multiple entities from Port.

```
DELETE https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-multiple-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-multiple-entities?connectionId=$CONNECTION_ID&entities%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entities[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-multiple-entities?${params}`, {
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
| `blueprintIdentifier` | string | no | The Port blueprint identifier. |
| `entities[]` | array<string> | yes | Entity identifiers to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedEntities": [
        "string"
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
| `deletedEntities` | array<string> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints/:blueprint_identifier/bulk/entities/delete` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-entities.md) for the provider-specific parameters and requirements.

