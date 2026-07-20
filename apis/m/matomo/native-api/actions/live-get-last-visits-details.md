# Live get Last Visits Details with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Live get Last Visits Details](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | no | Matomo API parameter. |
| `date` | body | `string` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `countVisitorsToFetch` | body | `string` | no | Matomo API parameter. |
| `minTimestamp` | body | `string` | no | Matomo API parameter. |
| `flat` | body | `boolean` | no | Matomo API parameter. |
| `doNotFetchActions` | body | `string` | no | Matomo API parameter. |
| `enhanced` | body | `string` | no | Matomo API parameter. |
