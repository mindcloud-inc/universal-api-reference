# Place Order using Webhook with PostcardMania

Creates a new order in PostcardMania using a webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/webhook/{{webhookID}}`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Place Order using Webhook](https://docs.pcmintegrations.com/docs/directmail-api/393aq3ihkf5ec)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookID` | path | `number` | yes | Preconfigured webhook identifier. |
