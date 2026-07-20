# Create Email List with Sendcrux

Creates a new email list in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/lists`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Create Email List](https://api.sendbound.com/email-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact[address_1]` | body | `string` | no | The primary street address for the list contact profile. |
| `contact[city]` | body | `string` | no | The city for the list contact profile. |
| `contact[company]` | body | `string` | no | The company name for the list contact profile. |
| `contact[country_id]` | body | `string` | no | The numeric country identifier for the list contact profile. |
| `contact[email]` | body | `string` | no | The contact email address for the list profile. |
| `contact[state]` | body | `string` | no | The state or region for the list contact profile. |
| `default_subject` | body | `string` | yes | The default subject line for campaigns that use this list. |
| `from_email` | body | `string` | yes | The sender email address for the list. |
| `from_name` | body | `string` | yes | The sender display name for the list. |
| `name` | body | `string` | yes | The display name of the list. |
| `send_welcome_email` | body | `string` | no | Set to 1 to send the Sendcrux welcome email to new subscribers. |
| `subscribe_confirmation` | body | `string` | no | Set to 1 to require confirmation when people subscribe. |
| `unsubscribe_notification` | body | `string` | no | Set to 1 to notify the list owner when someone unsubscribes. |
