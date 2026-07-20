# Get Supplier with Fatture in Cloud

Retrieves a supplier from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/entities/suppliers/:supplier_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Get Supplier](https://developers.fattureincloud.it/api-reference/#operation/getSupplier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `supplier_id` | path | `number` | yes | The ID of the supplier. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
