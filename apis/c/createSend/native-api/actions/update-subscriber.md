# Update Subscriber with CreateSend

Updates an existing subscriber in CreateSend by email address.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Update Subscriber](https://www.campaignmonitor.com/api/subscribers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | path | `string` | yes |
| `email` | query | `string` | yes |
| `EmailAddress` | body | `string` | no |
| `Name` | body | `string` | no |
| `Resubscribe` | body | `boolean` | no |
| `RestartSubscriptionBasedAutoresponders` | body | `boolean` | no |
| `ConsentToTrack` | body | `string` | no |
