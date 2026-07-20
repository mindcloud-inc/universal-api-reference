# Update Task with Insightly

Updates an existing task in Insightly.

## Endpoint

- **Method:** `PUT`
- **Path:** `{apiBaseUrl}Tasks`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Update Task](https://api.insightly.com/v3.1/Help#!/Tasks/UpdateEntity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TASK_ID` | body | `number` | yes |
| `TITLE` | body | `string` | yes |
| `DETAILS` | body | `string` | no |
| `DUE_DATE` | body | `string` | no |
| `STATUS` | body | `string` | no |
| `PRIORITY` | body | `number` | no |
| `COMPLETED` | body | `boolean` | yes |
| `PROJECT_ID` | body | `number` | no |
