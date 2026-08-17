# Get Sales Accrual Report with Zenoti

## Endpoint

- **Method:** `POST`
- **Path:** `reports/sales/accrual_basis/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [Get Sales Accrual Report](None)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `center_ids[].center` | body | `list` | no | — |
| `invoice_statuses[].invoiceStatus` | body | `list` | no | — |
| `item_types[].itemType` | body | `list` | no | — |
| `payment_types[].paymentType` | body | `list` | no | — |
| `sale_types[].saleType` | body | `list` | no | — |
| `start_date` | body | `date` | yes | — |
| `end_date` | body | `date` | yes | — |
| `center_ids[]` | body | `array` | no | — |
| `item_types[]` | body | `array` | no | — |
| `payment_types[]` | body | `array` | no | — |
| `sale_types[]` | body | `array` | no | — |
| `invoice_statuses[]` | body | `array` | no | — |
| `includeTotal` | body | `boolean` | no | Format: `toggle`. |
