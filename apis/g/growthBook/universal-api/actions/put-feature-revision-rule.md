# GrowthBook: Update a rule in a draft revision

Updates a rule in a GrowthBook feature revision.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "version": "1",
  "ruleId": "rule_1",
  "environment": "production",
  "rule": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/put-feature-revision-rule', {
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
    "environment": "production",
    "rule": {"sample":"value"}
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
| `environment` | string | yes | Default: `production`. |
| `rule` | object | yes | Default: `{"sample":"value"}`. |
| `rampSchedule` | object | no |  |
| `schedule` | object | no |  |
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

Through the native GrowthBook API, this operation is `PUT /features/:id/revisions/:version/rules/:ruleId` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-feature-revision-rule.md) for the provider-specific parameters and requirements.

