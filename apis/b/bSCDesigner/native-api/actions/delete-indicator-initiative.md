# Delete Indicator Initiative with BSC Designer

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Delete Indicator Initiative](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/removeInitiativeUsingDELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias |
| `guid` | path | `string` | yes | Indicator guid |
| `initiativeGuid` | path | `string` | yes | Initiative guid |
