# Add Attendance Entry by Punch In or Out with Zoho People

Creates attendance entries by punch direction in Zoho People.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/attendance/entries/:direction`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Add Attendance Entry by Punch In or Out](https://www.zoho.com/people/api/v3/attendance/entries-punch-in-or-out.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | path | `string` | yes | Punch direction. Use in or out. |
| `lattitude` | body | `string` | no | Latitude of the punch location. Zoho documents this parameter as lattitude. |
| `longitude` | body | `string` | no | Longitude of the punch location. |
| `accuracy` | body | `string` | no | Accuracy of the punch location. |
| `description` | body | `string` | no | Optional description to attach to the punch event. |
