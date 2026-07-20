# Action1: List Automation Instances

Retrieves automation instances from Action1 for an organization.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-automation-instances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-automation-instances?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-automation-instances?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": "string",
      "end_time": "string",
      "endpoint_results": "string",
      "endpoints": "string",
      "id": "string",
      "name": "Ava Chen",
      "percent_completed": "string",
      "retry_minutes": "string",
      "schedule": "string",
      "self": "string",
      "start_time": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | string |  |
| `end_time` | string |  |
| `endpoint_results` | string |  |
| `endpoints` | string |  |
| `id` | string |  |
| `name` | string |  |
| `percent_completed` | string |  |
| `retry_minutes` | string |  |
| `schedule` | string |  |
| `self` | string |  |
| `start_time` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /automations/instances/:orgId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-automation-instances.md) for the provider-specific parameters and requirements.

