# Get Indicator Initiative with BSC Designer

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Get Indicator Initiative](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/getInitiativeUsingGET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid containing the initiative. |
| `initiativeGuid` | path | `string` | yes | Initiative guid to retrieve. |
