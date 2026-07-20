# Event Cart Calculation with Explara

Retrieves an event cart calculation from Explara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/publisher/cart-calculation`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [Event Cart Calculation](https://apidocs.explara.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | body | `string` | yes | Explara event identifier. |
| `tickets[]` | body | `array<object>` | yes | Array of ticket selection objects. |
