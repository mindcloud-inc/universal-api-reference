# List Received Documents with Fatture in Cloud

Retrieves received documents from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/received_documents`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [List Received Documents](https://developers.fattureincloud.it/api-reference/#operation/listReceivedDocuments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `type` | query | `list` | yes | The type of the received document. Accepted values: `expense`, `passive_credit_note`, `passive_delivery_note`, `self_invoice`. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
| `q` | query | `string` | no | Query for filtering the results. |
