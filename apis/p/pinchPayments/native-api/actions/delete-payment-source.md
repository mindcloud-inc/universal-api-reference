# Delete Payment Source with Pinch Payments

Deletes a payment source from Pinch Payments.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/payers/[:id]/sources/[:sourceId]`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [Delete Payment Source](https://docs.getpinch.com.au/reference/delete-payment-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Payer ID in pyr_XXXXXXXXXXXXXX format. |
| `sourceId` | path | `string` | yes | Source ID in src_XXXXXXXXXXXXXX format. |
