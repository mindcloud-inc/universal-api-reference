# Get Selected Indicator Values with BSC Designer

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/api/document/:docId/kpi/batch/get-value/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Selected Indicator Values](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/getChosenValuesUsingPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document ID or alias. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
| `guids[]` | body | `array<string>` | yes | Array of indicator GUIDs. |
