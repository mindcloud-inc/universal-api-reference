# List Customers with VentiPay

Retrieves customers from VentiPay.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.ventipay.com/v1`
- **Official documentation:** [List Customers](https://docs.ventipay.com/reference/customers-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email del cliente. Debe ser coincidencia exacta. |
| `country` | query | `string` | no | País del cliente en formato ISO 3166-1 alpha-2. |
| `starting_after` | query | `string` | no | Return records after this pagination cursor from a previous response. |
| `ending_before` | query | `string` | no | Return records before this pagination cursor from a previous response. |
