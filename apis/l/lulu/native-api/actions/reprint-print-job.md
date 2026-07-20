# Reprint Print Job with Lulu

Creates a reprint of a print job in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/print-jobs/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Reprint Print Job](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_reprint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_email` | body | `string` | yes | Email contact for the Lulu reprint job. |
| `line_items[]` | body | `array` | yes | Array of Lulu reprint line items. |
| `shipping_address` | body | `object` | yes | Shipping address for the Lulu reprint job. |
| `shipping_level` | body | `string` | yes | Shipping level for the Lulu reprint job. |
