# Create Subscriber with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Create Subscriber](https://api.sender.net/subscribers/add-subscriber/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The value must be a valid email address. |
| `firstname` | body | `string` | no | Subscriber firstname. |
| `lastname` | body | `string` | no | Subscriber lastname. |
| `groups[]` | body | `array<string>` | no | Provide the new groups assigned to the subscriber. |
| `fields` | body | `object` | no | Provide field key-value pairs for the subscriber. |
| `phone` | body | `string` | no | Phone number must include the country code. |
| `trigger_automation` | body | `boolean` | no | Send false to avoid activating an automation. |
