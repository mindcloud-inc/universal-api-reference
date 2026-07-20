# Get Indicator Grouped Values with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/indicator/:guid/grouped-value/:period`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Indicator Grouped Values](https://www.webbsc.com/swagger-ui.html#/rest-kpi-grouped-values-controller/getByPeriodUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `guid` | path | `string` | yes | Indicator GUID. |
| `period` | path | `string` | yes | Grouping period: DAY, WEEK, MONTH, QUARTER, HALF_YEAR, or YEAR. |
