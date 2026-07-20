# GrowthBook: Create a single experimentTemplate

Creates a new experiment template in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-experiment-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-experiment-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateMetadata": {
    "sample": "value"
  },
  "type": "sample",
  "datasource": "sample",
  "exposureQueryId": "sample_id_1",
  "statsEngine": "sample",
  "targeting": {
    "sample": "value"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-experiment-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateMetadata": {"sample":"value"},
    "type": "sample",
    "datasource": "sample",
    "exposureQueryId": "sample_id_1",
    "statsEngine": "sample",
    "targeting": {"sample":"value"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | no |  |
| `templateMetadata` | object | yes | Default: `{"sample":"value"}`. |
| `type` | string | yes | Default: `sample`. |
| `hypothesis` | string | no |  |
| `description` | string | no |  |
| `tags` | list<string> | no |  |
| `customFields` | object | no |  |
| `datasource` | string | yes | Default: `sample`. |
| `exposureQueryId` | string | yes | Default: `sample_id_1`. |
| `hashAttribute` | string | no |  |
| `fallbackAttribute` | string | no |  |
| `disableStickyBucketing` | boolean | no |  |
| `goalMetrics` | list<string> | no |  |
| `secondaryMetrics` | list<string> | no |  |
| `guardrailMetrics` | list<string> | no |  |
| `activationMetric` | string | no |  |
| `statsEngine` | string | yes | Default: `sample`. |
| `segment` | string | no |  |
| `skipPartialData` | boolean | no |  |
| `targeting` | object | yes | Default: `{"sample":"value"}`. |
| `customMetricSlices[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "experimentTemplate": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `experimentTemplate` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /experiment-templates` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-experiment-template.md) for the provider-specific parameters and requirements.

