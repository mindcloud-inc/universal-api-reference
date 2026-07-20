# Restore draft email to editing with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-editing`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Restore draft email to editing](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `emailId` | path | `string` | yes | ID of the draft email |
