# GrowthBook: Create a single rampSchedule

Creates a new ramp schedule in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `featureId` | string | no | Feature that anchors this schedule. Required when ruleId/environment are set. |
| `ruleId` | string | no | Rule to attach as the initial target. Requires featureId and environment. |
| `environment` | string | no | Environment of the target rule. Requires featureId and ruleId. |
| `steps[]` | array<object> | no | Ordered ramp steps. When featureId+ruleId+environment are provided, `targetId` and `patch.ruleId` in actions are auto-injected — only supply the patch fields you want to change. |
| `endActions[]` | array<object> | no | Actions applied when the ramp completes. targetId and patch.ruleId are auto-injected when featureId+ruleId+environment are provided. |
| `startDate` | date | no |  |
| `endCondition` | object | no | Optional hard deadline |
| `templateId` | string | no | Load steps and endActions from a saved template (featureId+ruleId+environment must also be set for auto-injection) |

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

Through the native GrowthBook API, this operation is `POST /ramp-schedules` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ramp-schedule.md) for the provider-specific parameters and requirements.

