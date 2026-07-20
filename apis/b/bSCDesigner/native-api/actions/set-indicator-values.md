# Set Indicator Values with BSC Designer

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/api/document/:docId/kpi/indicator/:guid/value/:date`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Set Indicator Values](https://www.webbsc.com/swagger-ui.html#/rest-kpi-value-controller/setSingleValueUsingPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid to update. |
| `date` | path | `string` | yes | Date in yyyy-MM-dd format. |
| `value` | body | `number` | yes | Indicator value at the given date. |
| `target` | body | `number` | yes | Target at the given date. |
| `baseline` | body | `number` | yes | Baseline at the given date. |
| `min` | body | `number` | yes | Minimum at the given date. |
| `max` | body | `number` | yes | Maximum at the given date. |
