# Event Generate Order with Explara

Creates a new event order in Explara.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/publisher/generate-order`
- **Base URL:** `https://www.explara.com`
- **Official documentation:** [Event Generate Order](https://apidocs.explara.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | body | `string` | yes | Explara event identifier. |
| `tickets[]` | body | `array<object>` | yes | Array of ticket selection objects. |
