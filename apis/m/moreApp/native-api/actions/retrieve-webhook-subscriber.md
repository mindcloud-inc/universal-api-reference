# Retrieve Webhook Subscriber with MoreApp

Retrieves a webhook subscriber from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Webhook Subscriber](https://docs.moreapp.com/docs/developer-docs/07bc433ed2ba5-retrieve-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `subscriberId` | path | `string` | yes | MoreApp subscriber identifier. |
