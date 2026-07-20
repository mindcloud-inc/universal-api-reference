# Create order with i2i

Creates a new ship order in i2i.

## Endpoint

- **Method:** `POST`
- **Path:** `/ibis/api/v1.1/customers/{consumerTag}/ship/orders`
- **Base URL:** `https://exch.i2i.ca`
- **Official documentation:** [Create order](https://www.i2i.ca/why-i2i/our-software)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `header` | body | `object` | yes | Order header object matching the existing i2i connector payload: number, ref_no, po_no, service, shipper, soldto, shipto, and optional comments. |
| `lines[]` | body | `array<object>` | yes | Line item array matching the existing i2i connector payload. Each line includes description, item, and qty. |
