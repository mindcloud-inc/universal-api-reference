# Update Tax Data with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/:client/updateTaxData`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Update Tax Data](https://api-docs.invoicing.co/#tag/clients/operation/updateClientTaxData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client` | path | `string` | yes | Hashed client ID. |
| `address1` | body | `string` | yes | Street address used to refresh the client's tax data. |
| `city` | body | `string` | yes | City used to refresh the client's tax data. |
| `state` | body | `string` | yes | State or region used to refresh the client's tax data. |
| `postal_code` | body | `string` | yes | Postal code used to refresh the client's tax data. |
| `country_id` | body | `number` | yes | Country identifier used to refresh the client's tax data. |
