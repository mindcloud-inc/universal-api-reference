# Get Case Docket Entry with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/dockets/{docket_no}`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Get Case Docket Entry](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the docket entry. |
| `court_code` | path | `string` | yes | PACER court code for the docket entry. |
| `docket_no` | path | `string` | yes | Docket entry number within the case. |
