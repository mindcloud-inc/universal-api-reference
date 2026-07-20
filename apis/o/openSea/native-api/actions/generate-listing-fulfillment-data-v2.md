# Fulfill Listing with OpenSea

Retrieves listing fulfillment data from OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/listings/fulfillment_data`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Fulfill Listing](https://docs.opensea.io/reference/generate_listing_fulfillment_data_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listing` | body | `object` | yes | — |
| `fulfiller` | body | `object` | yes | — |
| `consideration` | body | `object` | no | — |
| `recipient` | body | `string` | no | — |
| `units_to_fill` | body | `number` | no | Optional quantity of units to fulfill; defaults to remaining units for listings |
| `include_optional_creator_fees` | body | `boolean` | no | Whether to include optional creator fees in the fulfillment. If creator fees are already required, this is a no-op. Defaults to false. |
