# Add Subscriber with Campaign Monitor

Adds a subscriber to a Campaign Monitor list, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Add Subscriber](https://www.campaignmonitor.com/api/v3-3/subscribers/#adding-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `EmailAddress` | body | `string` | yes | Subscriber email address. |
| `Name` | body | `string` | no | Subscriber name. |
| `Resubscribe` | body | `boolean` | no | Whether to resubscribe the subscriber if previously unsubscribed. |
| `ConsentToTrack` | body | `string` | no | Consent-to-track value for the subscriber. |
