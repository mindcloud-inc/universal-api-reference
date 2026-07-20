# Create Invoice with Starfish

Creates a new invoice in Starfish.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Create Invoice](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Invoice type: concept or invoice. |
| `status` | body | `string` | yes | Invoice status such as draft, unpaid, partly_paid, or paid. |
