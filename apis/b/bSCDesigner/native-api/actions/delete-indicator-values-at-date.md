# Delete Indicator Values At Date with BSC Designer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/api/document/:documentId/kpi/indicator/:indicatorGuid/values/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Delete Indicator Values At Date](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteValueAtUsingDELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document id containing the indicator values. |
| `indicatorGuid` | path | `string` | yes | Indicator guid whose values should be deleted. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
