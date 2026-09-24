# List Time Cards by Associate ID with ADP

Getting all presence time entries for an employee and for a given period.

## Endpoint

- **Method:** `GET`
- **Path:** `time/v2/workers/:employeeAOID/time-cards`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Time Cards by Associate ID](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn.next.gen/hcm-offrg-wfn.next.gen-time-time-cards-v2-time-cards?operation=GET%2Fevents%2Ftime%2Fv2%2Ftime-entries.modify%2F%7Bevent-id%7D#swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `employeeAOID` | path | `string` | yes |
