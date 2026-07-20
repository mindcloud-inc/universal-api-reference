# Delete Indicator Max At Date with BSC Designer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/api/document/:documentId/kpi/indicator/:indicatorGuid/max/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Delete Indicator Max At Date](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteMaxAtUsingDELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document id |
| `indicatorGuid` | path | `string` | yes | Indicator guid |
| `date` | path | `string` | yes | Date (yyyy-MM-dd) |
