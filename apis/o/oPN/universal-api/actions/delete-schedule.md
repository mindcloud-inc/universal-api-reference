# OPN: Delete Schedule

Deletes an existing schedule from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-schedule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-schedule?${params}`, {
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
| `id` | string | yes | The schedule ID to delete. |

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

Through the native OPN API, this operation is `DELETE /schedules/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-schedule.md) for the provider-specific parameters and requirements.

