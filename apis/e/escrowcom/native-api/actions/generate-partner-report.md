# Generate Partner Report with Escrow.com

Creates a partner report in Escrow.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner/reports`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Generate Partner Report](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_filters` | body | `object` | no | Transaction filters for generating the partner report. |
| `customer_filters` | body | `object` | no | Customer filters for generating the partner report. |
