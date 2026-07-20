# Update Subscriber with Buttondown

Updates an existing subscriber in Buttondown.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:id_or_email`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Update Subscriber](https://docs.buttondown.com/api-subscribers-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_or_email` | path | `string` | yes | Subscriber ID or email address. |
| `email_address` | body | `string` | no | Updated subscriber email address. |
| `notes` | body | `string` | no | Private notes attached to the subscriber. |
| `tags[]` | body | `array<string>` | no | Tags to replace on the subscriber. |
| `type` | body | `list` | no | Updated subscriber type. Accepted values: `gifted`, `regular`, `unpaid`, `unsubscribed`. |
| `commenting_disabled` | body | `boolean` | no | Whether commenting is disabled for the subscriber. |
