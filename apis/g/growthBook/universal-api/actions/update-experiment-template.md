# GrowthBook: Update a single experimentTemplate

Updates an existing experiment template in GrowthBook.

```
PUT https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-experiment-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-experiment-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/update-experiment-template', {
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
| `project` | string | no |  |
| `templateMetadata` | object | no |  |
| `type` | string | no |  |
| `hypothesis` | string | no |  |
| `description` | string | no |  |
| `tags` | list<string> | no |  |
| `customFields` | object | no |  |
| `datasource` | string | no |  |
| `exposureQueryId` | string | no |  |
| `hashAttribute` | string | no |  |
| `fallbackAttribute` | string | no |  |
| `disableStickyBucketing` | boolean | no |  |
| `goalMetrics` | list<string> | no |  |
| `secondaryMetrics` | list<string> | no |  |
| `guardrailMetrics` | list<string> | no |  |
| `activationMetric` | string | no |  |
| `statsEngine` | string | no |  |
| `segment` | string | no |  |
| `skipPartialData` | boolean | no |  |
| `targeting` | object | no |  |
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

Through the native GrowthBook API, this operation is `PUT /experiment-templates/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-experiment-template.md) for the provider-specific parameters and requirements.

