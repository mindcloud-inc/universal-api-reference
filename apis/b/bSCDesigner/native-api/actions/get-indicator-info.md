# Get Indicator Info with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/:guid`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Indicator Info](https://www.webbsc.com/swagger-ui.html#/rest-kpi-controller/getKpiUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `guid` | path | `string` | yes | Indicator GUID. |
