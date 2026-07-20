# Action1: List Endpoint Groups

Retrieves endpoint groups from Action1 for an organization.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-endpoint-groups?${params}`, {
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
| `orgId` | string | yes | Provide an organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contents": "string",
      "description": "string",
      "exclude_filter": "string",
      "exclude_filter_logic": "string",
      "id": "string",
      "include_filter": "string",
      "include_filter_logic": "string",
      "name": "Ava Chen",
      "self": "string",
      "type": "string",
      "uptime_alerts": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contents` | string |  |
| `description` | string |  |
| `exclude_filter` | string |  |
| `exclude_filter_logic` | string |  |
| `id` | string |  |
| `include_filter` | string |  |
| `include_filter_logic` | string |  |
| `name` | string |  |
| `self` | string |  |
| `type` | string |  |
| `uptime_alerts` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /endpoints/groups/:orgId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-endpoint-groups.md) for the provider-specific parameters and requirements.

