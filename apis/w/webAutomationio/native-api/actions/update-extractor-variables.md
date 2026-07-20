# Update Extractor Variables with WebAutomation.io

Updates one variable value for a specific extractor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/extractor_variables/{{EXTRACTOR_ID}}/`
- **Base URL:** `https://webautomation.io/api`
- **Official documentation:** [Update Extractor Variables](https://webautomation.io/api/redoc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EXTRACTOR_ID` | path | `number` | yes | The extractor ID. |
| `field_type` | body | `string` | no | The extractor variable field type. |
| `key` | body | `string` | yes | The extractor variable key to update. |
| `value` | body | `string` | yes | The value to assign to the extractor variable. |
