# Get Sales Report with Zenoti

## Endpoint

- **Method:** `POST`
- **Path:** `reports/sales/accrual_basis/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [Get Sales Report](None)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centres[].centre` | body | `list` | no | — |
| `invoice_statuses[].invoiceStatus` | body | `list` | no | — |
| `item_types[].itemType` | body | `list` | no | — |
| `payment_types[].paymentType` | body | `list` | no | — |
| `sale_types[].salesType` | body | `list` | no | — |
| `start_date` | body | `date` | no | — |
| `end_date` | body | `date` | no | — |
| `center_ids[]` | body | `array` | no | — |
| `sold_by_ids[]` | body | `array<string>` | no | Employee IDs |
| `item_types[]` | body | `array` | no | — |
| `payment_types[]` | body | `array` | no | — |
| `sale_types[]` | body | `array<object>` | no | — |
| `invoice_statuses[]` | body | `array<object>` | no | — |
| `includeTotal` | body | `boolean` | no | Format: `toggle`. |
