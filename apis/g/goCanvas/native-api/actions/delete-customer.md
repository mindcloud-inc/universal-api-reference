# Delete Customer with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Customer](https://api.gocanvas.com/api/v3/docs#delete-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently deletes the customer when true. Omit or set false for soft deletion. |
