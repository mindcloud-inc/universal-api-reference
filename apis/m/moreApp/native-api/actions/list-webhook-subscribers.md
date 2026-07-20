# List Webhook Subscribers with MoreApp

Retrieves webhook subscribers from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/subscribers`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [List Webhook Subscribers](https://docs.moreapp.com/docs/developer-docs/fe9894cd0a286-list-all-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
