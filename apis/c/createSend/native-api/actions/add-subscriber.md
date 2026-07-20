# Add Subscriber with CreateSend

Creates a new subscriber in CreateSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Add Subscriber](https://www.campaignmonitor.com/api/v3-3/subscribers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `EmailAddress` | body | `string` | yes |
| `Name` | body | `string` | no |
| `Resubscribe` | body | `boolean` | no |
| `ConsentToTrack` | body | `string` | no |
