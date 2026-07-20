# Update Subscriber with Sender

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:subscriberKey`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Update Subscriber](https://api.sender.net/subscribers/update-subscriber/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriberKey` | path | `string` | yes | Subscriber email address, phone number, or ID. |
| `firstname` | body | `string` | no | Updated first name. |
| `lastname` | body | `string` | no | Updated last name. |
| `groups[]` | body | `array<string>` | no | New groups assigned to the subscriber. |
| `fields` | body | `object` | no | Provide field key-value pairs for the subscriber. |
| `subscriber_status` | body | `string` | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. |
| `phone` | body | `string` | no | Phone number must include the country code. |
| `trigger_automation` | body | `boolean` | no | Send false to avoid activating an automation. |
| `sms_status` | body | `string` | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. |
| `transactional_email_status` | body | `string` | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. |
