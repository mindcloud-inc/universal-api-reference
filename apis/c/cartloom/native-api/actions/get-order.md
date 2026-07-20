# Get Order with Cartloom

Retrieves an order from Cartloom by invoice number.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/get/format/json`
- **Base URL:** `https://mindcloudstage0424.cartloom.com/api`
- **Official documentation:** [Get Order](https://support.cartloom.com/hc/en-us/articles/115000936188-Get-Order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `string` | yes | Invoice number of the order. |
| `email` | body | `string` | no | Customer email address. |
