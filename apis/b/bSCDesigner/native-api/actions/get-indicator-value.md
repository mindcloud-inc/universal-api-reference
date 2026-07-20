# Get Indicator Value with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/indicator/:guid/value/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Indicator Value](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getSingleValueUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `guid` | path | `string` | yes | Indicator GUID. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
