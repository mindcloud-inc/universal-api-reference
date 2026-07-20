# Update Event with WaiverFile

Updates an existing event in WaiverFile.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateEvent`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Update Event](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventID` | query | `string` | yes |
| `eventName` | query | `string` | yes |
| `dateStart` | query | `date` | yes |
| `dateEnd` | query | `date` | yes |
| `isAllDay` | query | `boolean` | yes |
| `eventCategoryID` | query | `string` | yes |
| `waiverFormIDs[]` | body | `array` | yes |
| `waiverFormIDs[]` | body | `array` | yes |
