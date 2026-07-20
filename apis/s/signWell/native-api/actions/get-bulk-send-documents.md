# Get Bulk Send Documents with SignWell

Retrieves documents for a bulk send in SignWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_sends/:id/documents`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Get Bulk Send Documents](https://developers.signwell.com/reference/get_api-v1-bulk-sends-id-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier for a bulk send. |
| `limit` | query | `number` | no | Number of documents to fetch. Defaults to 10, max is 50. |
| `page` | query | `number` | no | Page number for pagination. |
