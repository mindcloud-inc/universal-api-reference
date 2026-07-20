# Add Orders To Batch with Print.one Postcards

Adds orders to a batch in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/batches/:batchId/orders`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Add Orders To Batch](https://api.print.one/docs/v2#operation/Batch/addBatchOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID to add orders to |
| `mergeVariables` | body | `object` | yes | Personalization data as a JSON object |
| `recipient.name` | body | `string` | yes | Recipient name |
| `recipient.address` | body | `string` | yes | Recipient street address |
| `recipient.postalCode` | body | `string` | yes | Recipient postal code |
| `recipient.city` | body | `string` | yes | Recipient city |
| `recipient.country` | body | `string` | yes | Recipient country ISO code |
| `autoGenNextBatch` | body | `boolean` | no | Generate a new batch automatically when this one no longer accepts orders |
