# Search Court Cases with Court Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/courts/pacer/{court_code}/cases/search`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Search Court Cases](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `court_code` | path | `string` | yes | PACER court code for the search. |
