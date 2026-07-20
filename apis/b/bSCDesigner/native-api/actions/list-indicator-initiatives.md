# List Indicator Initiatives with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/:guid/initiatives`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [List Indicator Initiatives](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/getInitiativesUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid whose initiatives should be listed. |
