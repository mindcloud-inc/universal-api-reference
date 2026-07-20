# List Comment Attachments with Nozbe Personal

Retrieves attachments for a Nozbe Personal comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/:comment_id/attachments`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Comment Attachments](https://api4.nozbe.com/v1/api#/attachments/getattachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | Comment ID from Nozbe. |
