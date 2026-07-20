# Fulfill Offer with OpenSea

Retrieves offer fulfillment data from OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/offers/fulfillment_data`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Fulfill Offer](https://docs.opensea.io/reference/generate_offer_fulfillment_data_v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer` | body | `object` | yes | — |
| `fulfiller` | body | `object` | yes | — |
| `consideration` | body | `object` | no | — |
| `units_to_fill` | body | `number` | no | Optional quantity of units to fulfill; defaults to 1 for offers |
| `include_optional_creator_fees` | body | `boolean` | no | Whether to include optional creator fees in the fulfillment. If creator fees are already required, this is a no-op. Defaults to false. |
