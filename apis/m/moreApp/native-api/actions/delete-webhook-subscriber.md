# Delete Webhook Subscriber with MoreApp

Deletes a webhook subscriber from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Webhook Subscriber](https://docs.moreapp.com/docs/developer-docs/1dcc9c1c7b668-delete-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `subscriberId` | path | `string` | yes | MoreApp subscriber identifier. |
