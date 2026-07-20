# List Receipts with Aspire

Lists Aspire receipts using the available OData query parameters. Use this to find existing receipts and inspect fields such as status, invoice metadata, notes, received date, items, and costs. Aspire receipts cannot be updated after createReceipt; there is no updateReceipt endpoint or field-level patch action. The only post-create change path is approveReceipt, and it can add or change only the vendor invoice number and vendor invoice date. If the user wants to change any other field on an existing receipt, surface that constraint upfront and offer to recreate the receipt with the corrected values.

## Endpoint

- **Method:** `GET`
- **Path:** `Receipts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Receipts](https://guide.youraspire.com/apidocs/receipts-5)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
