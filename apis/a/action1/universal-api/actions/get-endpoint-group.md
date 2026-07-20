# Action1: Get Endpoint Group

Retrieves an endpoint group from Action1 by ID.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint-group?connectionId=$CONNECTION_ID&orgId=string&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-endpoint-group?${params}`, {
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
| `groupId` | string | yes | Provide an endpoint group ID. |

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

Through the native Action1 API, this operation is `GET /endpoints/groups/:orgId/:groupId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-endpoint-group.md) for the provider-specific parameters and requirements.

