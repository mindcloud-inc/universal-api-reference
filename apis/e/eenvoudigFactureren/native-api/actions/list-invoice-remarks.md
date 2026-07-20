# List Invoice Remarks with EenvoudigFactureren

Retrieves invoice remarks from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoice_id/remarks`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [List Invoice Remarks](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381977-api-facturen)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | EenvoudigFactureren invoice ID. |
