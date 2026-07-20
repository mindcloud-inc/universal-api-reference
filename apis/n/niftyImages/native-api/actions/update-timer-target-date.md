# Update Timer Target Date with NiftyImages

Updates a timer target date in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Timer/Update`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Timer Target Date](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TimerImageUrl` | body | `string` | yes | URL of the timer image to update. |
| `TargetDate` | body | `string` | yes | New timer target date in ISO 8601 format. |
| `Format` | body | `string` | no | Date format when TargetDate is not already ISO 8601. |
| `IsUtc` | body | `boolean` | no | Set to true to adjust the target date using the timer timezone. |
| `AddHours` | body | `number` | no | Hours to add to the target date. |
| `AddDays` | body | `number` | no | Days to add to the target date. |
| `AddMonths` | body | `number` | no | Months to add to the target date. |
