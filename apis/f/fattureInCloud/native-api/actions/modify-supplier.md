# Modify Supplier with Fatture in Cloud

Updates an existing supplier in Fatture in Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/c/:company_id/entities/suppliers/:supplier_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Modify Supplier](https://developers.fattureincloud.it/api-reference/#operation/modifySupplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `supplier_id` | path | `number` | yes | The ID of the supplier. |
| `data` | body | `object` | yes | The supplier payload inside the provider data envelope. |
