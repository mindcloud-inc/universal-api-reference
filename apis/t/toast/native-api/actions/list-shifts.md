# List Shifts with Toast

Retrieves labor shifts by identifier or by an ISO-8601 date range of up to one month.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/shifts`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [List Shifts](https://doc.toasttab.com/openapi/labor/operation/shiftsGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shiftIds` | query | `string` | no | One or more Toast GUIDs or external shift identifiers, with a maximum of 100. Send multiple values as a array. |
| `startDate` | query | `date` | no | Inclusive beginning of the shift date range in ISO-8601 format. |
| `endDate` | query | `date` | no | Exclusive end of the shift date range in ISO-8601 format. |
