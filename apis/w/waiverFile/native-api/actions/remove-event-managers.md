# Remove Event Managers with WaiverFile

Removes event managers from an event in WaiverFile.

## Endpoint

- **Method:** `POST`
- **Path:** `/RemoveEventManagers`
- **Base URL:** `https://api.waiverfile.com/api/v1`
- **Official documentation:** [Remove Event Managers](https://api.waiverfile.com/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventID` | query | `string` | yes |
| `emailAddresses` | query | `string` | yes |
