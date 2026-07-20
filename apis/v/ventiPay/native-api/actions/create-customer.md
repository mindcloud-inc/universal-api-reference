# Create Customer with VentiPay

Creates a new customer in VentiPay.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://api.ventipay.com/v1`
- **Official documentation:** [Create Customer](https://docs.ventipay.com/reference/customers-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email del cliente. |
| `country` | body | `string` | yes | Pais del cliente. |
| `first_name` | body | `string` | no | Primer nombre del cliente. |
| `last_name` | body | `string` | no | Apellido paterno del cliente. |
| `metadata` | body | `string` | no | Conjunto de pares llave-valor asociado al objeto. |
