# Add Timesheet with AssessTEAM

Creates a new timesheet entry in AssessTEAM.

## Endpoint

- **Method:** `POST`
- **Path:** `/timesheet/addtimesheet`
- **Base URL:** `https://restapi.assessteam.com`
- **Official documentation:** [Add Timesheet](https://restapi.assessteam.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectname` | query | `string` | yes | Project name, for example Acme Sample Project. |
| `personcode` | query | `string` | yes | Unique person code, for example 1001. |
| `timeby` | query | `string` | yes | Time by mode, either Time_by_Day or Time_by_Month. |
| `dateormonth` | query | `string` | yes | Date for day mode or month for month mode, for example Apr-2026. |
| `hours` | query | `number` | yes | Hours, for example 8.5. |
| `comment` | query | `string` | no | Optional comment for the timesheet entry. |
