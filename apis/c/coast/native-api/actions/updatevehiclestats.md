# Update Vehicle Stats with Coast

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/vehicles/telematics`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Vehicle Stats](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Vehicle telematics payloads to send to Coast. |
