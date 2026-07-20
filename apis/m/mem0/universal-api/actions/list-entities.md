# Mem0: List Entities

Retrieves entities from Mem0.

```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-entities?${params}`, {
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
| `entity_type` | string | no | Mem0 entity type filter when supported. |
| `org_id` | string | no | Mem0 organization ID filter when supported. |
| `project_id` | string | no | Mem0 project ID filter when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity_id": "string",
      "entity_type": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity_id` | string |  |
| `entity_type` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Mem0 API, this operation is `GET /v1/entities/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entities.md) for the provider-specific parameters and requirements.

