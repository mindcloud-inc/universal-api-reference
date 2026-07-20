# Create Webhook (Program) with Fidel API

Creates a webhook for a Fidel program.

## Endpoint

- **Method:** `POST`
- **Path:** `/programs/:programId/hooks`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create Webhook (Program)](https://reference.fidel.uk/reference/create-webhook-program)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `event` | body | `string` | yes | The webhook event type. |
| `url` | body | `string` | yes | URL destination of the event. |
| `offerId` | body | `string` | no | Optional offer ID filter for qualified auth and clearing transaction events. |
