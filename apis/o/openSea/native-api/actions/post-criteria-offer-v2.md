# Create Criteria Offer with OpenSea

Creates a criteria offer in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/offers`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Create Criteria Offer](https://docs.opensea.io/reference/post_criteria_offer_v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `protocol_data` | body | `object` | yes |
| `criteria` | body | `object` | yes |
| `protocol_address` | body | `string` | yes |
