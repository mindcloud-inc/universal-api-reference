# Statsig: Fully Update Experiment

Updates an experiment in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-experiment-post-console-v1-experiments-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-experiment-post-console-v1-experiments-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "description": "string",
  "idType": "string",
  "hypothesis": "string",
  "groups": "string",
  "allocation": 1,
  "targetingGateID": "string",
  "bonferroniCorrection": true,
  "defaultConfidenceInterval": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/fully-update-experiment-post-console-v1-experiments-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "description": "string",
    "idType": "string",
    "hypothesis": "string",
    "groups": "string",
    "allocation": 1,
    "targetingGateID": "string",
    "bonferroniCorrection": true,
    "defaultConfidenceInterval": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | id |
| `name` | string | no | Request body field. |
| `description` | string | yes | Request body field. |
| `idType` | string | yes | Request body field. |
| `secondaryIDType` | string | no | Request body field. |
| `identifierMappingMode` | string | no | Request body field. |
| `identityResolutionSource` | string | no | Request body field. |
| `hypothesis` | string | yes | Request body field. |
| `links` | list | no | Request body field. |
| `externalEvents` | list | no | Request body field. |
| `groups` | list | yes | Request body field. |
| `controlGroupID` | string | no | Request body field. |
| `allocation` | number | yes | Request body field. |
| `userBuckets` | list | no | Request body field. |
| `primaryMetricTags` | list | no | Request body field. |
| `secondaryMetricTags` | list | no | Request body field. |
| `primaryMetrics` | list | no | Request body field. |
| `secondaryMetrics` | list | no | Request body field. |
| `otherMetrics` | list | no | Request body field. |
| `targetApps` | string | no | Request body field. |
| `tags` | list | no | Request body field. |
| `duration` | number | no | Request body field. |
| `targetExposures` | number | no | Request body field. |
| `targetingGateID` | string | yes | Request body field. |
| `sequentialTesting` | boolean | no | Request body field. |
| `bonferroniCorrection` | boolean | yes | Request body field. |
| `bonferroniCorrectionPerMetric` | boolean | no | Request body field. |
| `benjaminiHochbergPerVariant` | boolean | no | Request body field. |
| `benjaminiHochbergPerMetric` | boolean | no | Request body field. |
| `benjaminiPrimaryMetricsOnly` | boolean | no | Request body field. |
| `defaultConfidenceInterval` | string | yes | Request body field. |
| `defaultRollupWindow` | number | no | Request body field. |
| `defaultChanceToBeatThreshold` | number | no | Request body field. |
| `bayesianPriors` | list | no | Request body field. |
| `manualQualityScores` | list | no | Request body field. |
| `status` | string | yes | Request body field. |
| `launchedGroupID` | string | no | Request body field. |
| `assignmentSourceName` | string | no | Request body field. |
| `assignmentSourceExperimentName` | string | no | Request body field. |
| `creatorID` | string | no | Request body field. |
| `creatorEmail` | string | no | Request body field. |
| `isAnalysisOnly` | boolean | no | Request body field. |
| `team` | string | no | Request body field. |
| `teamID` | string | no | Request body field. |
| `allocationDuration` | number | no | Request body field. |
| `cohortedAnalysisDuration` | number | no | Request body field. |
| `cohortedMetricsMatureAfterEnd` | boolean | no | Request body field. |
| `cohortWaitUntilEndToInclude` | boolean | no | Request body field. |
| `fixedAnalysisDuration` | number | no | Request body field. |
| `scheduledReloadHour` | number | no | Request body field. |
| `scheduledReloadType` | string | no | Request body field. |
| `scheduledReloadDays` | list | no | Request body field. |
| `turboMode` | boolean | no | Request body field. |
| `analysisEndTime` | string | no | Request body field. |
| `assignmentSourceFilters` | list | no | Request body field. |
| `analyticsType` | string | no | Request body field. |
| `defaultSPRTPowerParam` | number | no | Request body field. |
| `defaultSPRTMDE` | number | no | Request body field. |
| `sprtBaselineMode` | string | no | Request body field. |
| `sprtMDESettings` | list | no | Request body field. |
| `isSidecar` | boolean | no | Request body field. |
| `decisionReason` | string | no | Request body field. |
| `preComputedUserDimensions` | list | no | Request body field. |
| `cureCovariates` | list | no | Request body field. |
| `stratifiedSampling` | object | no | Request body field. |
| `enabledNonProdEnvironments` | list | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/experiments/{id}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fully-update-experiment-post-console-v1-experiments-id.md) for the provider-specific parameters and requirements.

