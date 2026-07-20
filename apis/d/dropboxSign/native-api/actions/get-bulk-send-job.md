# Get Bulk Send Job with Dropbox Sign

Retrieves a bulk send job from Dropbox Sign by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_send_job/:bulk_send_job_id`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Get Bulk Send Job](https://developers.hellosign.com/api/reference/operation/bulkSendJobGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulk_send_job_id` | path | `string` | yes | The ID of the Bulk Send Job to retrieve. |
| `page` | query | `number` | no | Which page number of the Bulk Send Job to return. |
| `page_size` | query | `number` | no | Number of objects to return per page. |
