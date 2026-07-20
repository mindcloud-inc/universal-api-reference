# Build Criteria Offer with OpenSea

Builds a criteria offer in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/offers/build`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Build Criteria Offer](https://docs.opensea.io/reference/build_offer_v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offerer` | body | `string` | yes |
| `quantity` | body | `number` | yes |
| `criteria` | body | `object` | yes |
| `protocol_address` | body | `string` | yes |
| `offer_protection_enabled` | body | `boolean` | yes |
