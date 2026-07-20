# Get Excel Report with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/report/:id/excel`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Excel Report](https://www.webbsc.com/swagger-ui.html#/report-controller/getExcelReportAtDateForRestUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Report or document ID. |
| `start` | query | `string` | no | Optional report date in yyyy-MM-dd format. |
