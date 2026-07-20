# Create Task with Insightly

Creates a new task in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Tasks`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Task](https://api.insightly.com/v3.1/Help#!/Tasks/AddEntity)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `TITLE` | body | `string` | yes |
| `DETAILS` | body | `string` | no |
| `DUE_DATE` | body | `string` | no |
| `STATUS` | body | `string` | no |
| `PRIORITY` | body | `number` | no |
| `COMPLETED` | body | `boolean` | yes |
| `PROJECT_ID` | body | `number` | no |
