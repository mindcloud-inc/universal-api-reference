# Resource Guru: List Resources

Retrieves resources from Resource Guru.

```
GET https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources?${params}`, {
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
      "booking_approver_ids": [
        1
      ],
      "color": "string",
      "created_at": "string",
      "creator_id": 1,
      "first_name": "Ava",
      "historical_timezones": [
        {}
      ],
      "id": 1,
      "last_name": "Chen",
      "last_updated_by": "string",
      "name": "Ava Chen",
      "rate_id": 1,
      "resource_type": {},
      "should_submit_timesheets_from": "string",
      "timesheet_approver_ids": [
        1
      ],
      "timezone": {},
      "type": "string",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking_approver_ids` | array<number> |  |
| `color` | string |  |
| `created_at` | string |  |
| `creator_id` | number |  |
| `first_name` | string |  |
| `historical_timezones` | array<object> |  |
| `id` | number |  |
| `last_name` | string |  |
| `last_updated_by` | string |  |
| `name` | string |  |
| `rate_id` | number |  |
| `resource_type` | object |  |
| `should_submit_timesheets_from` | string |  |
| `timesheet_approver_ids` | array<number> |  |
| `timezone` | object |  |
| `type` | string |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Resource Guru API, this operation is `GET /resources` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resources.md) for the provider-specific parameters and requirements.

