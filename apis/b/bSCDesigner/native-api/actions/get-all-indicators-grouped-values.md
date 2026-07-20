# Get All Indicators Grouped Values with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/indicatos/grouped-value/:period`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get All Indicators Grouped Values](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getBatchByPeriodUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `period` | path | `string` | yes | Grouping period: DAY, WEEK, MONTH, QUARTER, HALF_YEAR, or YEAR. |
