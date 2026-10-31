# Delete Person Certification Attachment with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Certification Attachment](https://developers.gobridgit.com/reference/personcertattachments_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `certId` | path | `number` | yes | The certification ID |
| `id` | path | `number` | yes | The attachment ID |
