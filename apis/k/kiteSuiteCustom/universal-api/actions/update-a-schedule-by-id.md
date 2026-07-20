# Kite Suite: Update a schedule by ID



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-schedule-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-schedule-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "name": "Ava Chen",
  "timeFrom": "string",
  "timeTo": "string",
  "activeDays[]": [
    "string"
  ],
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-schedule-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "name": "Ava Chen",
    "timeFrom": "string",
    "timeTo": "string",
    "activeDays[]": ["string"],
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the schedule to update. |
| `body` | object | yes | Request body |
| `name` | string | yes | The name of the schedule. |
| `timeFrom` | string | yes | Start time for the schedule. |
| `timeTo` | string | yes | End time for the schedule. |
| `activeDays[]` | array | yes | List of active days for the schedule. |
| `timezone` | string | yes | Timezone of the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "activeDays": [
        "string"
      ],
      "name": "Ava Chen",
      "timeFrom": "string",
      "timeTo": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `activeDays` | array<string> |  |
| `name` | string |  |
| `timeFrom` | string |  |
| `timeTo` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/campaign/schedule/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-schedule-by-id.md) for the provider-specific parameters and requirements.

