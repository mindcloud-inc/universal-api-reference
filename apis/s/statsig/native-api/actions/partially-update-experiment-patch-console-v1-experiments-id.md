# Partially Update Experiment with Statsig

Updates an experiment in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/experiments/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially Update Experiment](https://docs.statsig.com/api-reference/experiments/partially-update-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `idType` | body | `string` | no | Request body field. |
| `secondaryIDType` | body | `string` | no | Request body field. |
| `identifierMappingMode` | body | `string` | no | Request body field. |
| `identityResolutionSource` | body | `string` | no | Request body field. |
| `hypothesis` | body | `string` | no | Request body field. |
| `links` | body | `list` | no | Request body field. |
| `externalEvents` | body | `list` | no | Request body field. |
| `groups` | body | `list` | no | Request body field. |
| `controlGroupID` | body | `string` | no | Request body field. |
| `allocation` | body | `number` | no | Request body field. |
| `userBuckets` | body | `list` | no | Request body field. |
| `primaryMetricTags` | body | `list` | no | Request body field. |
| `secondaryMetricTags` | body | `list` | no | Request body field. |
| `primaryMetrics` | body | `list` | no | Request body field. |
| `secondaryMetrics` | body | `list` | no | Request body field. |
| `otherMetrics` | body | `list` | no | Request body field. |
| `targetApps` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `duration` | body | `number` | no | Request body field. |
| `targetExposures` | body | `number` | no | Request body field. |
| `targetingGateID` | body | `string` | no | Request body field. |
| `sequentialTesting` | body | `boolean` | no | Request body field. |
| `bonferroniCorrection` | body | `boolean` | no | Request body field. |
| `bonferroniCorrectionPerMetric` | body | `boolean` | no | Request body field. |
| `benjaminiHochbergPerVariant` | body | `boolean` | no | Request body field. |
| `benjaminiHochbergPerMetric` | body | `boolean` | no | Request body field. |
| `benjaminiPrimaryMetricsOnly` | body | `boolean` | no | Request body field. |
| `defaultConfidenceInterval` | body | `string` | no | Request body field. |
| `defaultRollupWindow` | body | `number` | no | Request body field. |
| `defaultChanceToBeatThreshold` | body | `number` | no | Request body field. |
| `bayesianPriors` | body | `list` | no | Request body field. |
| `manualQualityScores` | body | `list` | no | Request body field. |
| `status` | body | `string` | no | Request body field. |
| `launchedGroupID` | body | `string` | no | Request body field. |
| `assignmentSourceName` | body | `string` | no | Request body field. |
| `assignmentSourceExperimentName` | body | `string` | no | Request body field. |
| `creatorID` | body | `string` | no | Request body field. |
| `creatorEmail` | body | `string` | no | Request body field. |
| `isAnalysisOnly` | body | `boolean` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `allocationDuration` | body | `number` | no | Request body field. |
| `cohortedAnalysisDuration` | body | `number` | no | Request body field. |
| `cohortedMetricsMatureAfterEnd` | body | `boolean` | no | Request body field. |
| `cohortWaitUntilEndToInclude` | body | `boolean` | no | Request body field. |
| `fixedAnalysisDuration` | body | `number` | no | Request body field. |
| `scheduledReloadHour` | body | `number` | no | Request body field. |
| `scheduledReloadType` | body | `string` | no | Request body field. |
| `scheduledReloadDays` | body | `list` | no | Request body field. |
| `turboMode` | body | `boolean` | no | Request body field. |
| `analysisEndTime` | body | `string` | no | Request body field. |
| `assignmentSourceFilters` | body | `list` | no | Request body field. |
| `analyticsType` | body | `string` | no | Request body field. |
| `defaultSPRTPowerParam` | body | `number` | no | Request body field. |
| `defaultSPRTMDE` | body | `number` | no | Request body field. |
| `sprtBaselineMode` | body | `string` | no | Request body field. |
| `sprtMDESettings` | body | `list` | no | Request body field. |
| `isSidecar` | body | `boolean` | no | Request body field. |
| `decisionReason` | body | `string` | no | Request body field. |
| `preComputedUserDimensions` | body | `list` | no | Request body field. |
| `cureCovariates` | body | `list` | no | Request body field. |
| `stratifiedSampling` | body | `object` | no | Request body field. |
| `enabledNonProdEnvironments` | body | `list` | no | Request body field. |
