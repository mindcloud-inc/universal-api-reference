# Get Collections Report with Zenoti

## Endpoint

- **Method:** `POST`
- **Path:** `reports/collections/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`
- **Official documentation:** [Get Collections Report](https://linear.app/mindcloud/issue/MC-1685/create-the-zenoti-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centers.ids[]` | body | `array<object>` | no | — |
| `centers.ids[].center` | body | `list` | no | — |
| `invoice_statuses[].invoiceStatus` | body | `list` | no | — |
| `payment_types[].paymentType` | body | `list` | no | — |
| `sale_types[].salesType` | body | `list` | no | — |
| `start_date` | body | `date` | no | — |
| `centers.is_all` | body | `boolean` | no | Format: `toggle`. |
| `centers.type` | body | `list` | no | Format: `toggle`. |
| `end_date` | body | `date` | no | — |
| `centers` | body | `object` | no | — |
| `payment_types[]` | body | `array` | no | — |
| `sale_types[]` | body | `array<object>` | no | — |
| `invoice_statuses[]` | body | `array<object>` | no | — |
