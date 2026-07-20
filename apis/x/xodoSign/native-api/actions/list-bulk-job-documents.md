# List Bulk Job Documents with Xodo Sign

Retrieves documents from a bulk job in Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_job/:bulkSendingJobId/documents`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [List Bulk Job Documents](https://eversign.com/api/documentation/methods#get-bulk-job-documents-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkSendingJobId` | path | `number` | yes | The bulk sending job ID to retrieve documents for. |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the bulk job. |
| `limit` | query | `number` | no | Maximum amount of documents to fetch. |
| `offset` | query | `number` | no | Number of documents to skip when fetching results. |
