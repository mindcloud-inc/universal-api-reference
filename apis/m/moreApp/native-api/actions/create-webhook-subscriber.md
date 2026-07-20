# Create Webhook Subscriber with MoreApp

Creates a webhook subscriber in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Webhook Subscriber](https://docs.moreapp.com/docs/developer-docs/fea134e0e69b2-create-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `name` | body | `string` | yes | Subscriber display name. |
| `secret` | body | `string` | no | Optional signing secret. |
| `status` | body | `string` | yes | Subscriber status. |
| `type[]` | body | `array<string>` | yes | Webhook event types. Send multiple values as a array. |
| `url` | body | `string` | yes | Webhook URL to receive MoreApp events. |
