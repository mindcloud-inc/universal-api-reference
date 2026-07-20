# List Case Filers with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/filers`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [List Case Filers](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the filers list. |
| `court_code` | path | `string` | yes | PACER court code for the filers list. |
