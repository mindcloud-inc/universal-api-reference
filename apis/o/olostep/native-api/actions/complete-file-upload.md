# Complete File Upload with Olostep

Completes a file upload in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files/[:file_id]/complete`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Complete File Upload](https://docs.olostep.com/api-reference/files/complete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The ID of the uploaded file to finalize. |
