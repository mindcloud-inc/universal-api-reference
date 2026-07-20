# Update Offer with Fidel API

Updates an existing offer in Fidel API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/offers/:offerId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Update Offer](https://reference.fidel.uk/reference/edit-offer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerId` | path | `string` | yes | — |
| `name` | body | `string` | no | The offer name. |
| `shortDescription` | body | `string` | no | A short description for the offer. |
| `activation.enabled` | body | `boolean` | no | Whether activation is enabled. |
| `activation.qualifiedTransactionsLimit` | body | `number` | no | The number of qualified transactions required before the offer is redeemed. |
