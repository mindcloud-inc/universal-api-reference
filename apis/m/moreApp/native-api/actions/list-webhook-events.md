# List Webhook Events with MoreApp

Retrieves webhook events from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/events`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Webhook Events](https://docs.moreapp.com/docs/developer-docs/4e9b52015e45f-list-all-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `page` | query | `string` | no | Optional event page number. |
| `size` | query | `string` | no | Optional page size. |
| `type` | query | `string` | no | Optional webhook event type filter. |
