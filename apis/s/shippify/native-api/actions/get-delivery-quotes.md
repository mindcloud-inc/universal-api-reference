# Get Delivery Quotes with Shippify

Retrieves delivery quotes from Shippify for up to 100 deliveries.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/pricing/quotes/available`
- **Base URL:** `https://api.shippify.co`
- **Official documentation:** [Get Delivery Quotes](https://docs.shippify.co/developers/en/shippify-api/deliveries/delivery-quotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `number` | no | Optional Shippify company identifier where the deliveries would be created. |
| `type` | body | `string` | no | Optional Shippify delivery type such as slot, express, or flex. |
| `deliveries[]` | body | `array<object>` | yes | Required array of Shippify delivery payload objects using the documented pickup, dropoff, packages, referenceId, tags, extraData, and cod structure. |
