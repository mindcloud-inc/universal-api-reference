# Delete Indicator Target At Date with BSC Designer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/api/document/:documentId/kpi/indicator/:indicatorGuid/target/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Delete Indicator Target At Date](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/deleteTargetAtUsingDELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | Document id |
| `indicatorGuid` | path | `string` | yes | Indicator guid |
| `date` | path | `string` | yes | Date (yyyy-MM-dd) |
