# List Webhook Invocations with MoreApp

Retrieves webhook invocations from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}/invocations`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Webhook Invocations](https://docs.moreapp.com/docs/developer-docs/92dd591d20e9b-list-all-invocations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `subscriberId` | path | `string` | yes |
