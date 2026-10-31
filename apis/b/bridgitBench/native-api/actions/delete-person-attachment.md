# Delete Person Attachment with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/attachments/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Attachment](https://developers.gobridgit.com/reference/personattachments_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID |
| `personId` | path | `number` | yes | The person ID |
| `id` | path | `number` | yes | The attachment ID |
