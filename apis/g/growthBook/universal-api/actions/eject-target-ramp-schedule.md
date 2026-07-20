# GrowthBook: Remove a target rule from a ramp schedule

Removes a target rule from a GrowthBook ramp schedule.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/eject-target-ramp-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/eject-target-ramp-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/eject-target-ramp-schedule', {
  method: 'POST',
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
| `targetId` | string | no | Target ID (from the targets array) |
| `ruleId` | string | no | Rule ID — use with environment as an alternative to targetId |
| `environment` | string | no | Environment — use with ruleId as an alternative to targetId |

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

Through the native GrowthBook API, this operation is `POST /ramp-schedules/:id/actions/eject-target` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/eject-target-ramp-schedule.md) for the provider-specific parameters and requirements.

