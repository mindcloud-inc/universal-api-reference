# Create Indicator Initiative with BSC Designer

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/api/document/:docId/kpi/:guid/initiatives`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Create Indicator Initiative](https://www.webbsc.com/swagger-ui.html#/rest-kpi-initiative-controller/createInitiativeUsingPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `docId` | path | `string` | yes | Document id or alias containing the indicator. |
| `guid` | path | `string` | yes | Indicator guid for the new initiative. |
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
