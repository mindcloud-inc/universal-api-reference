# GrowthBook: Create a single experiment

Creates a new experiment in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-experiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-experiment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingKey": "sample",
  "name": "sample",
  "variations[]": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-experiment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingKey": "sample",
    "name": "sample",
    "variations[]": ["sample"],
    "variations[]": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasourceId` | string | no | ID for the [DataSource](#tag/DataSource_model). Can only be set if a templateId is not provided. |
| `assignmentQueryId` | string | no | The ID property of one of the assignment query objects associated with the datasource. Can only be set if a templateId is not provided. |
| `trackingKey` | string | yes | Default: `sample`. |
| `bypassDuplicateKeyCheck` | boolean | no | If true, allow creating an experiment even if another experiment with the same tracking key already exists |
| `name` | string | yes | Name of the experiment Default: `sample`. |
| `type` | string | no |  |
| `project` | string | no | Project ID which the experiment belongs to |
| `templateId` | string | no | ID of the [ExperimentTemplate](#tag/ExperimentTemplate_model) this experiment was created from. Template fields are applied by default and overridden by explicitly provided payload fields. |
| `hypothesis` | string | no | Hypothesis of the experiment |
| `description` | string | no | Description of the experiment |
| `tags` | list<string> | no |  |
| `metrics` | list<string> | no |  |
| `secondaryMetrics` | list<string> | no |  |
| `guardrailMetrics` | list<string> | no |  |
| `activationMetric` | string | no | Users must convert on this metric before being included |
| `segmentId` | string | no | Only users in this segment will be included |
| `queryFilter` | string | no | WHERE clause to add to the default experiment query |
| `owner` | string | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `archived` | boolean | no |  |
| `status` | string | no |  |
| `autoRefresh` | boolean | no |  |
| `hashAttribute` | string | no |  |
| `fallbackAttribute` | string | no |  |
| `hashVersion` | number | no |  |
| `disableStickyBucketing` | boolean | no |  |
| `bucketVersion` | number | no |  |
| `minBucketVersion` | number | no |  |
| `releasedVariationId` | string | no |  |
| `excludeFromPayload` | boolean | no |  |
| `inProgressConversions` | string | no |  |
| `attributionModel` | string | no | Setting attribution model to `"experimentDuration"` is the same as selecting "Ignore Conversion Windows" for the Conversion Window Override. Setting it to `"lookbackOverride"` requires a `lookbackOverride` object to be provided. |
| `lookbackOverride` | object | no | Controls the lookback override for the experiment. For type "window", value must be a non-negative number and valueUnit is required. |
| `statsEngine` | string | no |  |
| `variations[]` | array<object> | yes | Default: `["sample"]`. |
| `variations[]` | array<object> | yes | Default: `["sample"]`. |
| `phases[]` | array<object> | no |  |
| `phases[]` | array<object> | no |  |
| `regressionAdjustmentEnabled` | boolean | no | Controls whether regression adjustment (CUPED) is enabled for experiment analyses |
| `sequentialTestingEnabled` | boolean | no | Only applicable to frequentist analyses |
| `sequentialTestingTuningParameter` | number | no |  |
| `shareLevel` | string | no |  |
| `banditScheduleValue` | number | no |  |
| `banditScheduleUnit` | string | no |  |
| `banditBurnInValue` | number | no |  |
| `banditBurnInUnit` | string | no |  |
| `banditConversionWindowValue` | number | no |  |
| `banditConversionWindowUnit` | string | no |  |
| `postStratificationEnabled` | boolean | no | When null, the organization default is used. |
| `decisionFrameworkSettings` | object | no | Controls the decision framework and metric overrides for the experiment. Replaces the entire stored object on update (does not patch individual fields). |
| `metricOverrides[]` | array<object> | no | Per-metric analysis overrides for this experiment. Replaces the entire stored array (does not patch individual entries). |
| `metricOverrides[]` | array<object> | no | Per-metric analysis overrides for this experiment. Replaces the entire stored array (does not patch individual entries). |
| `defaultDashboardId` | string | no | ID of the default dashboard for this experiment. |
| `customFields` | object | no |  |
| `customMetricSlices[]` | array<object> | no | Custom slices that apply to ALL applicable metrics in the experiment |
| `customMetricSlices[]` | array<object> | no | Custom slices that apply to ALL applicable metrics in the experiment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "experiment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `experiment` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /experiments` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-experiment.md) for the provider-specific parameters and requirements.

