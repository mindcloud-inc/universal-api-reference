# AbTesting update Experiment with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [AbTesting update Experiment](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idExperiment` | body | `string` | yes | Matomo API parameter. |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | yes | Matomo API parameter. |
| `hypothesis` | body | `string` | yes | Matomo API parameter. |
| `variations` | body | `string` | yes | Matomo API parameter. |
| `confidenceThreshold` | body | `string` | yes | Matomo API parameter. |
| `mdeRelative` | body | `string` | yes | Matomo API parameter. |
| `percentageParticipants` | body | `string` | yes | Matomo API parameter. |
| `successMetrics` | body | `string` | yes | Matomo API parameter. |
| `includedTargets` | body | `string` | yes | Matomo API parameter. |
| `excludedTargets` | body | `string` | no | Matomo API parameter. |
| `startDate` | body | `string` | no | Matomo API parameter. |
| `endDate` | body | `string` | no | Matomo API parameter. |
| `forwardUtmParams` | body | `string` | no | Matomo API parameter. |
| `forwardAllQueryParams` | body | `string` | no | Matomo API parameter. |
