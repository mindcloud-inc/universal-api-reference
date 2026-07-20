# Get Indicator Values At Date with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:documentId/kpi/indicator/:indicatorGuid/values/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Indicator Values At Date](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getValueAtUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document ID. |
| `indicatorGuid` | path | `string` | yes | Indicator GUID. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
