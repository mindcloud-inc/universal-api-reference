# Get Hebrew Birthdays with Hebcal

Retrieves Hebrew birthdays from Hebcal.

## Endpoint

- **Method:** `POST`
- **Path:** `/yahrzeit`
- **Base URL:** `https://www.hebcal.com`
- **Official documentation:** [Get Hebrew Birthdays](https://www.hebcal.com/home/1705/yahrzeit-anniversary-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `n1` | body | `string` | no | Optional name for the person. |
| `y1` | body | `string` | yes | Gregorian birth year. |
| `m1` | body | `string` | yes | Gregorian birth month. |
| `d1` | body | `string` | yes | Gregorian birth day. |
| `s1` | body | `string` | no | Set on if the birth occurred after sunset. |
| `years` | body | `string` | no | How many Hebrew years to calculate. |
| `start` | body | `string` | no | Starting Hebrew year for calculations. |
| `end` | body | `string` | no | Ending Hebrew year for calculations. |
| `hebdate` | body | `string` | no | Append Hebrew date to event titles. |
