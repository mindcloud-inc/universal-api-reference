# Place Postcard Order with PostcardMania

Creates a new postcard order in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/postcard`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Place Postcard Order](https://docs.pcmintegrations.com/docs/directmail-api/24b58db675dad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designID` | body | `string` | no | Existing approved design to use for the postcard order. |
| `front` | body | `object` | no | Front artwork object when not using designID. |
| `mailClass` | body | `string` | no | One of FirstClass or Standard. |
| `recipients[]` | body | `array<object>` | no | Recipient array. Validation requires 1 to 50000 items. |
| `size` | body | `string` | no | Required when designID is omitted. One of 46, 46S, 58, 68, 69, 611, 651. |
| `back` | body | `object` | no | Back design payload when designID is not supplied. |
