# Register an Endpoint with DocuPipe

Registers a webhook endpoint in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/generate-endpoint`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Register an Endpoint](https://docs.docupipe.ai/reference/generate_endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL of the webhook endpoint |
| `subscribedEvents[]` | body | `array<string>` | no | The events to subscribe to, if not specified, all events will be sent to the endpoint |
