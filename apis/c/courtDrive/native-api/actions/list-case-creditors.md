# List Case Creditors with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/creditors`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [List Case Creditors](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the creditors list. |
| `court_code` | path | `string` | yes | PACER court code for the creditors list. |
