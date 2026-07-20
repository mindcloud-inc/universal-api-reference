# List Case Claims with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/claims`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [List Case Claims](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the claims list. |
| `court_code` | path | `string` | yes | PACER court code for the claims list. |
