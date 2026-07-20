# Create Print Job with Lulu

Creates a new print job in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/print-jobs/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Create Print Job](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_email` | body | `string` | yes | Email contact for the Lulu print job. |
| `line_items[]` | body | `array` | yes | Array of Lulu print job line items. |
| `shipping_address` | body | `object` | yes | Shipping address for the Lulu print job. |
| `shipping_level` | body | `string` | yes | Shipping level for the Lulu print job. |
