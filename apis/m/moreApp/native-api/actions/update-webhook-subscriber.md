# Update Webhook Subscriber with MoreApp

Updates a webhook subscriber in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Webhook Subscriber](https://docs.moreapp.com/docs/developer-docs/fb9dac850ba59-update-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `name` | body | `string` | yes | Subscriber display name. |
| `secret` | body | `string` | no | Optional signing secret. |
| `status` | body | `string` | yes | Subscriber status. |
| `subscriberId` | path | `string` | yes | MoreApp subscriber identifier. |
| `type[]` | body | `array<string>` | yes | Webhook event types. Send multiple values as a array. |
| `url` | body | `string` | yes | Webhook URL to receive MoreApp events. |
