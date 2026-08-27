# Create Project Task with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/:wse/:endpointVersion/ProjectTask`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create Project Task](https://github.com/Acumatica/AcumaticaRESTAPIClientForCSharp/blob/6.0/EndpointDefinitions/Default_24.200.001)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wse` | path | `string` | yes | — |
| `endpointVersion` | path | `string` | yes | — |
| `ProjectID` | body | `object` | no | — |
| `ProjectID.value` | body | `string` | yes | — |
| `ProjectTaskID` | body | `object` | no | — |
| `ProjectTaskID.value` | body | `string` | yes | Acumatica community evidence shows this value can fail when it contains a hyphen. |
| `Description` | body | `object` | no | — |
| `Description.value` | body | `string` | no | — |
| `VisibilitySettings` | body | `object` | no | — |
| `VisibilitySettings.GL` | body | `object` | no | — |
| `VisibilitySettings.GL.value` | body | `boolean` | no | — |
| `VisibilitySettings.AP` | body | `object` | no | — |
| `VisibilitySettings.AP.value` | body | `boolean` | no | — |
| `VisibilitySettings.CRM` | body | `object` | no | — |
| `VisibilitySettings.CRM.value` | body | `boolean` | no | — |
| `VisibilitySettings.Expenses` | body | `object` | no | — |
| `VisibilitySettings.Expenses.value` | body | `boolean` | no | — |
| `VisibilitySettings.IN` | body | `object` | no | — |
| `VisibilitySettings.IN.value` | body | `boolean` | no | — |
| `VisibilitySettings.PO` | body | `object` | no | — |
| `VisibilitySettings.PO.value` | body | `boolean` | no | — |
| `VisibilitySettings.SO` | body | `object` | no | — |
| `VisibilitySettings.SO.value` | body | `boolean` | no | — |
| `VisibilitySettings.TimeEntries` | body | `object` | no | — |
| `VisibilitySettings.TimeEntries.value` | body | `boolean` | no | — |
| `VisibilitySettings.AR` | body | `object` | no | — |
| `VisibilitySettings.AR.value` | body | `boolean` | no | — |
| `VisibilitySettings.CA` | body | `object` | no | — |
| `VisibilitySettings.CA.value` | body | `boolean` | no | — |
