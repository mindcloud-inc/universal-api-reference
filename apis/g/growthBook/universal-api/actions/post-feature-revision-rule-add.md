# GrowthBook: Add a rule to a draft revision

Adds a rule to a GrowthBook feature revision.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature-revision-rule-add
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature-revision-rule-add" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "version": "1",
  "environment": "production",
  "rule": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-feature-revision-rule-add', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "version": "1",
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

Through the native GrowthBook API, this operation is `POST /features/:id/revisions/:version/rules` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-feature-revision-rule-add.md) for the provider-specific parameters and requirements.

