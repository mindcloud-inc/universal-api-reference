# Get All Indicator Values For Document with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/batch/all/get-value/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get All Indicator Values For Document](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getAllValuesUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
