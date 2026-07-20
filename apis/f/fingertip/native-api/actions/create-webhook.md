# Create Webhook with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Webhook](https://docs.fingertip.com/openapi-specs/create-webhook.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpointUrl` | body | `string` | yes | Webhook destination URL. |
| `triggers[]` | body | `array<object>` | yes | Webhook trigger definitions. |
