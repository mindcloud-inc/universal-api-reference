# Get Case Claim with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/claims/{claim_no}`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Get Case Claim](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the claim. |
| `claim_no` | path | `string` | yes | Claim entry number within the case. |
| `court_code` | path | `string` | yes | PACER court code for the claim. |
