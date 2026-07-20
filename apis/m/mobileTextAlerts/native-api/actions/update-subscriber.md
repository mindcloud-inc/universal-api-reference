# Update Subscriber with Mobile Text Alerts

Updates an existing subscriber in Mobile Text Alerts.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:idOrNumberOrEmail`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [Update Subscriber](https://developers.mobile-text-alerts.com/api-reference/subscribers#patch-subscribers-idornumberoremail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrNumberOrEmail` | path | `string` | yes | Subscriber ID, phone number, or email. |
| `email` | body | `string` | no | Updated subscriber email address. |
| `number` | body | `string` | no | Updated subscriber phone number. |
| `firstName` | body | `string` | no | Updated subscriber first name. |
| `lastName` | body | `string` | no | Updated subscriber last name. |
| `groupIds` | body | `string` | no | Comma-separated Mobile Text Alerts group IDs. |
