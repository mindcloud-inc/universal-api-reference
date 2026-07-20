# Create asset with UiPath Orchestrator

## Endpoint

- **Method:** `POST`
- **Path:** `/odata/Assets`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Create asset](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Asset name. |
| `ValueScope` | body | `string` | yes | Asset scope, usually Global. |
| `ValueType` | body | `string` | yes | Asset value type, such as Text, Bool, Integer, or Credential. |
| `StringValue` | body | `string` | no | Text value for Text assets. |
