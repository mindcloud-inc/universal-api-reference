# Get Person Certification Attachment with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:certId/attachments/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Get Person Certification Attachment](https://developers.gobridgit.com/reference/personcertattachments_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `certId` | path | `number` | yes | The certification ID |
| `id` | path | `number` | yes | The attachment ID |
