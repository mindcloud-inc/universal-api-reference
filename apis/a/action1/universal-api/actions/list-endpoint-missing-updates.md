# Action1: List Endpoint Missing Updates

Retrieves missing updates from Action1 for a specific endpoint.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-missing-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-missing-updates?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string&endpointId=endpoint-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string",
  "endpointId": "endpoint-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-missing-updates?${params}`, {
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
| `orgId` | string | yes | Action1 organization ID. |
| `endpointId` | string | yes | Managed endpoint ID. Example: `endpoint-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "builtin": "string",
      "description": "string",
      "id": "string",
      "internal_notes": "string",
      "kb_number": "string",
      "name": "Ava Chen",
      "optional": "string",
      "reboot_needed": "string",
      "recommended": "string",
      "scope": "string",
      "self": "string",
      "size": "string",
      "status": "string",
      "type": "string",
      "update_type": "string",
      "vendor": "string",
      "versions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builtin` | string |  |
| `description` | string |  |
| `id` | string |  |
| `internal_notes` | string |  |
| `kb_number` | string |  |
| `name` | string |  |
| `optional` | string |  |
| `reboot_needed` | string |  |
| `recommended` | string |  |
| `scope` | string |  |
| `self` | string |  |
| `size` | string |  |
| `status` | string |  |
| `type` | string |  |
| `update_type` | string |  |
| `vendor` | string |  |
| `versions` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /endpoints/managed/:orgId/:endpointId/missing-updates` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-endpoint-missing-updates.md) for the provider-specific parameters and requirements.

