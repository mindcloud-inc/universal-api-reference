# Search PACER Case by Number with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/cases/pacer/search/case_no/{case_number}`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Search PACER Case by Number](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_number` | path | `string` | yes | PACER case number to search. |
