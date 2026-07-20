# Retrieve Lead Deletion Request with Unbounce

Retrieves a lead deletion request from Unbounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:page_id/lead_deletion_request/:lead_deletion_request_id`
- **Base URL:** `https://api.unbounce.com`
- **Official documentation:** [Retrieve Lead Deletion Request](https://developer.unbounce.com/api_reference/#id_pages__page_id__lead_deletion_request__lead_deletion_request_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_deletion_request_id` | path | `string` | yes | Lead deletion request ID. |
| `page_id` | path | `string` | yes | Unbounce page ID. |
