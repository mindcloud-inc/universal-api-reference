# GrowthBook: Set ramp schedule for a rule

Sets a ramp schedule for a GrowthBook rule.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule-ramp-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule-ramp-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "version": "1",
  "ruleId": "rule_1",
  "environment": "production"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule-ramp-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "version": "1",
    "ruleId": "rule_1",
    "environment": "production"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `version` | number | yes | Default: `1`. |
| `ruleId` | string | yes | Default: `rule_1`. |
| `name` | string | no |  |
| `templateId` | string | no |  |
| `steps[]` | array<object> | no |  |
| `steps[]` | array<object> | no |  |
| `endActions[]` | array<object> | no |  |
| `endActions[]` | array<object> | no |  |
| `startDate` | string | no |  |
| `endCondition` | object | no |  |
| `environment` | string | yes | Default: `production`. |
| `revisionTitle` | string | no |  |
| `revisionComment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revision": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revision` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `PUT /features/:id/revisions/:version/rules/:ruleId/ramp-schedule` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-feature-revision-rule-ramp-schedule.md) for the provider-specific parameters and requirements.

