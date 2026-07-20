# OPN: Create Schedule

Creates a new schedule in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "charge": {},
      "created_at": "string",
      "deleted": true,
      "deleted_by": "string",
      "end_on": "string",
      "ended_at": "string",
      "every": 1,
      "execute_time": "string",
      "id": "string",
      "in_words": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "next_occurrences_on": [
        "string"
      ],
      "object": "string",
      "occurrences": {},
      "on": {},
      "period": "string",
      "start_on": "string",
      "state": "string",
      "status": "string",
      "transfer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `charge` | object |  |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `deleted_by` | string |  |
| `end_on` | string |  |
| `ended_at` | string |  |
| `every` | number |  |
| `execute_time` | string |  |
| `id` | string |  |
| `in_words` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `next_occurrences_on` | array<string> |  |
| `object` | string |  |
| `occurrences` | object |  |
| `on` | object |  |
| `period` | string |  |
| `start_on` | string |  |
| `state` | string |  |
| `status` | string |  |
| `transfer` | object |  |

## Native endpoint

Through the native OPN API, this operation is `POST /schedules` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schedule.md) for the provider-specific parameters and requirements.

