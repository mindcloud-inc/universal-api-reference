# Set Indicator Info with BSC Designer

## Endpoint

- **Method:** `PUT`
- **Path:** `/rest/api/document/:docId/kpi/:guid`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Set Indicator Info](https://www.webbsc.com/swagger-ui.html#/rest-kpi-controller/setKpiUsingPUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid to update. |
| `name` | body | `string` | yes | Updated indicator name. |
| `description` | body | `string` | no | Updated indicator description. |
| `indicatorType` | body | `string` | yes | Indicator type. |
