# Send Document with Billingo

Sends a document to email recipients in Billingo.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/send`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Send Document](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Billingo document ID to send. |
| `emails[]` | body | `array<string>` | no | Email addresses to receive the document. Send multiple values as a array. |
