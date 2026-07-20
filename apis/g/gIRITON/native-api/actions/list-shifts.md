# List Shifts with GIRITON

Retrieves a list of shifts from GIRITON.

## Endpoint

- **Method:** `GET`
- **Path:** `/shift/shifts`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Shifts](https://rest.giriton.com/apidoc/#/Shift/getShifts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `validSince` | query | `string` | no | Valid since date for shifts. |
| `validUntil` | query | `string` | no | Valid until date for shifts. |
