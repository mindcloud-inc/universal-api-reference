# Set Selected Indicator Values with BSC Designer

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/api/document/:docId/kpi/batch/set-value/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Set Selected Indicator Values](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/setChosenValuesUsingPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicators. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
| `values` | body | `list<object>` | yes | Array of indicator value payloads shaped like the provider RestKpiSetValue model. |
