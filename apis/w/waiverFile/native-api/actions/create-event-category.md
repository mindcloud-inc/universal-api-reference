# Create Event Category with WaiverFile

Creates a new event category in WaiverFile.

## Endpoint

- **Method:** `POST`
- **Path:** `/InsertEventCategory`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Create Event Category](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | yes |
| `active` | query | `boolean` | yes |
