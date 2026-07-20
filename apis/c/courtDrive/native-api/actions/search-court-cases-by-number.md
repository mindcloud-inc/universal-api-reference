# Search Court Cases by Number with Court Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/courts/pacer/{court_code}/cases/search/by-case-number`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Search Court Cases by Number](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_no` | body | `string` | yes | Case number to search for in the selected court. |
| `court_code` | path | `string` | yes | PACER court code for the search. |
