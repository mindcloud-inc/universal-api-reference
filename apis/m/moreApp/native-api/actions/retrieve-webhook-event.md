# Retrieve Webhook Event with MoreApp

Retrieves a webhook event from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/webhooks/customer/{{customerId}}/events/{{eventId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Retrieve Webhook Event](https://docs.moreapp.com/docs/developer-docs/d69445f35889b-retrieve-an-event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `eventId` | path | `string` | yes |
