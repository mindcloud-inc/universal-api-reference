# Update Event Category with WaiverFile

Updates an existing event category in WaiverFile.

## Endpoint

- **Method:** `POST`
- **Path:** `/UpdateEventCategory`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Update Event Category](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventCategoryID` | query | `string` | yes |
| `name` | query | `string` | yes |
| `active` | query | `boolean` | yes |
