# Get Punch Audit with Paycom

The Get method returns historical information for an employee's punches in a given date range. This method defaults to the current pay period of the employee. Date range may not exceed 30 days.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/employee/:eecode/punchaudit`
- **Base URL:** `https://api.paycomonline.net/v4/rest/index.php/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audittype` | query | `list` | no | — |
| `eecode` | path | `string` | yes | — |
| `startdate` | query | `date` | no | This is the start date of the request in UNIX format. |
| `enddate` | query | `date` | no | This is the end date of the request in UNIX format. |
