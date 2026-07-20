# Create Subscriber with Mobile Text Alerts

Creates a new subscriber in Mobile Text Alerts.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [Create Subscriber](https://developers.mobile-text-alerts.com/api-reference/subscribers#post-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Subscriber email address. |
| `number` | body | `string` | no | Subscriber phone number. |
| `firstName` | body | `string` | no | Subscriber first name. |
| `lastName` | body | `string` | no | Subscriber last name. |
| `groupIds` | body | `string` | no | Comma-separated Mobile Text Alerts group IDs. |
| `welcomeMessage` | body | `string` | no | Optional welcome message to send after opt-in. |
