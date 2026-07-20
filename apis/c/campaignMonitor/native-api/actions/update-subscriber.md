# Update Subscriber with Campaign Monitor

Updates an existing subscriber in a Campaign Monitor list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Update Subscriber](https://www.campaignmonitor.com/api/v3-3/subscribers/#updating-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `email` | query | `string` | yes | Subscriber email address to update. |
| `EmailAddress` | body | `string` | no | New subscriber email address. |
| `Name` | body | `string` | no | Subscriber name. |
| `Resubscribe` | body | `boolean` | no | Whether to resubscribe the subscriber if previously unsubscribed. |
| `RestartSubscriptionBasedAutoresponders` | body | `boolean` | no | Whether to restart subscription-based autoresponders. |
| `ConsentToTrack` | body | `string` | no | Consent-to-track value for the subscriber. |
