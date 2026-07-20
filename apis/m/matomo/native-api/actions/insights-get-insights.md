# Insights get Insights with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Insights get Insights](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `reportUniqueId` | body | `string` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `limitIncreaser` | body | `string` | no | Matomo API parameter. |
| `limitDecreaser` | body | `string` | no | Matomo API parameter. |
| `filterBy` | body | `string` | no | Matomo API parameter. |
| `minImpactPercent` | body | `string` | no | Matomo API parameter. |
| `minGrowthPercent` | body | `string` | no | Matomo API parameter. |
| `comparedToXPeriods` | body | `string` | no | Matomo API parameter. |
| `orderBy` | body | `string` | no | Matomo API parameter. |
