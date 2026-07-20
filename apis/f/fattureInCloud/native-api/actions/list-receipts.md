# List Receipts with Fatture in Cloud

Retrieves receipts from Fatture in Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/receipts`
- **Base URL:** `https://api-v2.fattureincloud.it`
- **Official documentation:** [List Receipts](https://developers.fattureincloud.it/api-reference/#operation/listReceipts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | The ID of the company. |
| `fields` | query | `string` | no | List of comma-separated fields. |
| `fieldset` | query | `list` | no | Name of the fieldset. Accepted values: `basic`, `detailed`, `fic_view`. |
| `q` | query | `string` | no | Query for filtering the results. |
