# Copy Offer with Edoobox

Copies an existing offer in Edoobox, with or without dates.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/:offer_id/copy`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Copy Offer](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer_id` | path | `string` | yes | Source edoobox offer ID to copy. |
| `category` | body | `string` | yes | Target edoobox category ID for the copied offer. |
| `number` | body | `string` | yes | Offer number for the copied offer. |
| `copy_dates` | body | `boolean` | no | Whether to copy the source offer dates. |
| `date_start` | body | `string` | no | Start datetime for copied dates. |
