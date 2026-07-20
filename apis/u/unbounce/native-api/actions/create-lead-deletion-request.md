# Create Lead Deletion Request with Unbounce

Creates an asynchronous lead deletion request in Unbounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/:page_id/lead_deletion_request`
- **Base URL:** `https://api.unbounce.com`
- **Official documentation:** [Create Lead Deletion Request](https://developer.unbounce.com/api_reference/#id_pages__page_id__lead_deletion_request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_ids` | body | `string` | no | Lead IDs to delete |
| `page_id` | path | `string` | yes | Unbounce page ID. |
