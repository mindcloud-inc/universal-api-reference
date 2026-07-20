# Delete Lead Comment with noCRM.io

Deletes an existing lead comment from noCRM.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/leads/:lead_id/comments/:id`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Delete Lead Comment](https://www.nocrm.io/api#delete-a-comment-on-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Lead ID. |
| `id` | path | `string` | yes | Comment ID. |
