# Update Subscriber Email with Maildroppa

Updates a subscriber email address in Maildroppa.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscribers/email/{subscriberId}`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Update Subscriber Email](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newEmailAddress` | body | `string` | no | New email address to set. |
| `subscriberId` | path | `string` | yes | UUID of the subscriber. |
