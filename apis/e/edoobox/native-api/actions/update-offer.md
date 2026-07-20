# Update Offer with Edoobox

Updates an existing offer in Edoobox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/offer/:offer_id`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Update Offer](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer_id` | path | `string` | yes | edoobox offer ID. |
| `vat` | body | `string` | yes | Offer VAT mode to set on the offer. |
