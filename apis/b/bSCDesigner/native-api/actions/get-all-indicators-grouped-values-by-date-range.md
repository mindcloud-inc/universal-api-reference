# Get All Indicators Grouped Values By Date Range with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/indicators/grouped-value/:period/:startDate/:endDate`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get All Indicators Grouped Values By Date Range](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getBatchByPeriodAndDatesUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `period` | path | `string` | yes | Grouping period: DAY, WEEK, MONTH, QUARTER, HALF_YEAR, or YEAR. |
| `startDate` | path | `string` | yes | Start date in yyyy-MM-dd format. |
| `endDate` | path | `string` | yes | End date in yyyy-MM-dd format. |
