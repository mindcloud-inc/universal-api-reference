# Restore draft email to drafts with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-draft`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Restore draft email to drafts](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `emailId` | path | `string` | yes | ID of the draft email |
