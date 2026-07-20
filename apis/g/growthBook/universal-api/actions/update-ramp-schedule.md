# GrowthBook: Update a single rampSchedule

Updates an existing ramp schedule in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-ramp-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-ramp-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-ramp-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `name` | string | no |  |
| `steps[]` | array<object> | no |  |
| `endActions[]` | array<object> | no |  |
| `startDate` | date | no |  |
| `endCondition` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rampSchedule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rampSchedule` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `PUT /ramp-schedules/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ramp-schedule.md) for the provider-specific parameters and requirements.

