# Mem0: Delete Entity

Deletes an entity from Mem0.

```
DELETE https://connect.mindcloud.co/v1/universal/mem0/latest/actions/delete-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/delete-entity?connectionId=$CONNECTION_ID&entity_type=string&entity_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity_type": "string",
  "entity_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/delete-entity?${params}`, {
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
| `entity_type` | string | yes | Mem0 entity type from the entity resource path. |
| `entity_id` | string | yes | Mem0 entity ID from the entity resource path. |

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

Through the native Mem0 API, this operation is `DELETE /v2/entities/:entity_type/:entity_id/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entity.md) for the provider-specific parameters and requirements.

