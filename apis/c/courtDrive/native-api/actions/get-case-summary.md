# Get Case Summary with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/{court_code}/{case_number}/case_summary`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Get Case Summary](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number for the case summary. |
| `court_code` | path | `string` | yes | PACER court code for the case summary. |
