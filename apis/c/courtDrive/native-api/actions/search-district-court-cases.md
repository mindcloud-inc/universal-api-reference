# Search District Court Cases with Court Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/courts/pacer/{court_code}/cases/search/district`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Search District Court Cases](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `court_code` | path | `string` | yes | PACER district court code for the search. |
