# GrowthBook: Create a fact metric analysis

Creates a fact metric analysis in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric-analysis" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-metric-analysis', {
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
| `id` | string | yes | The fact metric id to analyze Default: `prj_19g6smo332up7`. |
| `userIdType` | string | no | The identifier type to use for the analysis. If not provided, defaults to the first available identifier type in the fact table. |
| `lookbackDays` | number | no | Number of days to look back for the analysis. Defaults to 30. |
| `populationType` | string | no | The type of population to analyze. Defaults to 'factTable', meaning the analysis will return the metric value for all units found in the fact table. |
| `populationId` | string | no |  |
| `additionalNumeratorFilters` | list<string> | no | We support passing in adhoc filters for an analysis that don't live on the metric itself. These are in addition to the metric's filters. To use this, you can pass in an array of Fact Table Filter Ids. |
| `additionalDenominatorFilters` | list<string> | no | We support passing in adhoc filters for an analysis that don't live on the metric itself. These are in addition to the metric's filters. To use this, you can pass in an array of Fact Table Filter Ids. |
| `useCache` | boolean | no | Whether to use a cached query if one exists. Defaults to true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metricAnalysis": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metricAnalysis` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /fact-metrics/:id/analysis` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-fact-metric-analysis.md) for the provider-specific parameters and requirements.

