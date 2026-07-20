# Create Subscriber with Buttondown

Creates a new subscriber in Buttondown.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Create Subscriber](https://docs.buttondown.com/api-subscribers-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | body | `string` | yes | Subscriber email address. |
| `notes` | body | `string` | no | Private notes attached to the subscriber. |
| `tags[]` | body | `array<string>` | no | Tags to add when creating the subscriber. |
| `type` | body | `list` | no | Subscriber type to create. Accepted values: `gifted`, `regular`, `unpaid`, `unsubscribed`. |
| `ip_address` | body | `string` | no | Original subscriber IP for spam validation. |
| `bypass_firewall` | body | `boolean` | no | Trusted-source only. Sends Buttondown's firewall-bypass header instead of passing this field upstream in the request body. |
