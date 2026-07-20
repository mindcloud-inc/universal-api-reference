# Delete Supplier with Fatture in Cloud

Deletes an existing supplier from Fatture in Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/c/:company_id/entities/suppliers/:supplier_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Delete Supplier](https://developers.fattureincloud.it/api-reference/#operation/deleteSupplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `supplier_id` | path | `number` | yes | The ID of the supplier. |
