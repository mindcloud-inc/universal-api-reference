# Delete Indicator Score At Date with BSC Designer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/api/document/:documentId/kpi/indicator/:indicatorGuid/score/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Delete Indicator Score At Date](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteScoreAtUsingDELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document id |
| `indicatorGuid` | path | `string` | yes | Indicator guid |
| `date` | path | `string` | yes | Date (yyyy-MM-dd) |
