# Get Receipt with Fatture in Cloud

Retrieves a receipt from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/receipts/:document_id`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [Get Receipt](https://developers.fattureincloud.it/api-reference/#operation/getReceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `document_id` | path | `number` | yes | The ID of the document. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
