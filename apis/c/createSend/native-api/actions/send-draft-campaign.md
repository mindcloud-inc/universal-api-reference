# Send Draft Campaign with CreateSend

Sends a draft campaign in CreateSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/send.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Send Draft Campaign](https://www.campaignmonitor.com/api/v3-3/campaigns/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignId` | path | `string` | yes |
| `ConfirmationEmail` | body | `string` | yes |
| `SendDate` | body | `string` | yes |
