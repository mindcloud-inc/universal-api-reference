# ChargeDesk: List Agent Activity

Retrieves agent activity logs from ChargeDesk.

```
GET https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-agent-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeDesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-agent-activity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-agent-activity?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "action_params": true,
      "action_reason": "string",
      "action_type": "string",
      "company": "string",
      "context": "string",
      "description": "string",
      "event": "string",
      "ip": "string",
      "object_id": "string",
      "object_type": "string",
      "occurred": 1,
      "params": "string",
      "source": "string",
      "sub_description": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_params` | boolean |  |
| `action_reason` | string |  |
| `action_type` | string |  |
| `company` | string |  |
| `context` | string |  |
| `description` | string |  |
| `event` | string |  |
| `ip` | string |  |
| `object_id` | string |  |
| `object_type` | string |  |
| `occurred` | number |  |
| `params` | string |  |
| `source` | string |  |
| `sub_description` | string |  |

## Native endpoint

Through the native ChargeDesk API, this operation is `GET /log/activity` (base URL `https://api.chargedesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agent-activity.md) for the provider-specific parameters and requirements.

