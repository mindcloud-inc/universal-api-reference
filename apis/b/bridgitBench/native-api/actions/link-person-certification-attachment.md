# Link Person Certification Attachment with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Link Person Certification Attachment](https://developers.gobridgit.com/reference/personcertattachments_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `certId` | path | `number` | yes | The certification ID |
| `attachmentId` | body | `number` | yes | — |
