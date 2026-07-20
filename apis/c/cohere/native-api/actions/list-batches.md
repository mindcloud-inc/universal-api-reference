# List Batches with Cohere

Lists batch jobs in Cohere.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/batches`
- **Base URL:** `https://api.cohere.com`
- **Official documentation:** [List Batches](https://docs.cohere.com/reference/list-batches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | query | `number` | no | Maximum number of batch jobs to return. |
| `page_token` | query | `string` | no | Pagination token returned by a previous list request. |
