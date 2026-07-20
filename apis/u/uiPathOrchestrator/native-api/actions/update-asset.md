# Update asset with UiPath Orchestrator

## Endpoint

- **Method:** `PUT`
- **Path:** `/odata/Assets(:id)`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Update asset](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric asset ID. |
| `Name` | body | `string` | yes | Asset name. |
| `ValueScope` | body | `string` | yes | Asset scope, usually Global. |
| `ValueType` | body | `string` | yes | Asset value type, such as Text, Bool, Integer, or Credential. |
| `StringValue` | body | `string` | no | Text value for Text assets. |
