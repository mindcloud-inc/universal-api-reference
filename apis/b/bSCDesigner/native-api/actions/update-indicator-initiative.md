# Update Indicator Initiative with BSC Designer

## Endpoint

- **Method:** `PUT`
- **Path:** `/rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Update Indicator Initiative](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/updateInitiativeUsingPUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid containing the initiative. |
| `initiativeGuid` | path | `string` | yes | Initiative guid to update. |
| `name` | body | `string` | yes | Initiative name. |
| `description` | body | `string` | no | Initiative description. |
| `status` | body | `string` | yes | Initiative status. |
| `showOnMap` | body | `boolean` | no | Whether the initiative should be shown on the map. |
| `initiativeType` | body | `string` | yes | Initiative type. |
| `budget` | body | `number` | no | Planned budget. |
| `currency` | body | `string` | no | Budget currency. |
| `duration` | body | `number` | no | Planned duration. |
| `durationUnit` | body | `string` | no | Duration unit. |
| `intervalStart` | body | `string` | no | Initiative start date. |
