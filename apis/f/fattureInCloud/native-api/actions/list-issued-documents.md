# List Issued Documents with Fatture in Cloud

Retrieves issued documents from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/issued_documents`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [List Issued Documents](https://developers.fattureincloud.it/api-reference/#operation/listIssuedDocuments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `type` | query | `list` | yes | The type of the issued document. Accepted values: `credit_note`, `delivery_note`, `invoice`, `order`, `proforma`, `quote`, `receipt`, `self_own_invoice`, `self_supplier_invoice`, `supplier_order`, `work_report`. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
| `q` | query | `string` | no | Query for filtering the results. |
| `inclusive` | query | `number` | no | (Only for type = delivery_notes) Include invoices delivery notes. |
