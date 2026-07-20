# CallScaler: List Number Group Members

Retrieves number group members from CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-number-group-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-number-group-members?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/list-number-group-members?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_flow_id": "string",
      "call_flow_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "friendly_name": "Ava Chen",
      "group_id": "string",
      "group_name": "Ava Chen",
      "id": "string",
      "phone_number": "string",
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
| `call_flow_id` | string | Assigned call flow ID. |
| `call_flow_name` | string | Assigned call flow name. |
| `created_at` | date | Tracking number creation timestamp. |
| `friendly_name` | string | Friendly name for the tracking number. |
| `group_id` | string | Assigned number group ID. |
| `group_name` | string | Assigned number group name. |
| `id` | string | Unique tracking number ID. |
| `phone_number` | string | Tracking phone number. |
| `status` | string | Tracking number status. |
| `type` | string | Number type. |

## Native endpoint

Through the native CallScaler API, this operation is `GET /number-groups/:id/members` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-number-group-members.md) for the provider-specific parameters and requirements.

