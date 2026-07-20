# Get Yahrzeit Dates with Yizkor with Hebcal

Retrieves yahrzeit dates with Yizkor from Hebcal.

## Endpoint

- **Method:** `POST`
- **Path:** `/yahrzeit`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Yahrzeit Dates with Yizkor](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `n1` | body | `string` | no | Optional name for the person. |
| `y1` | body | `string` | yes | Gregorian year of death. |
| `m1` | body | `string` | yes | Gregorian month of death. |
| `d1` | body | `string` | yes | Gregorian day of death. |
| `s1` | body | `string` | no | Set on if the event occurred after sunset. |
| `years` | body | `string` | no | How many Hebrew years to calculate. |
| `hebdate` | body | `string` | no | Append Hebrew date to event titles. |
| `i` | body | `string` | no | Use Israel Yizkor schedule when enabled. |
