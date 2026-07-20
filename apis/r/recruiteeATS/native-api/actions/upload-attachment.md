# Upload Attachment with Recruitee ATS

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/attachments`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Upload Attachment](https://docs.recruitee.com/reference/attachments-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment.remote_file_url` | body | `string` | yes | Public URL to the attachment file. |
| `attachment.candidate_id` | body | `number` | no | Candidate ID that should receive the attachment. |
| `attachment.offer_id` | body | `number` | no | Offer ID that should receive the attachment. |
