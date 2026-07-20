# Pause or Resume Campaign with VoiceGenie

Updates a campaign's running state in VoiceGenie.

## Endpoint

- **Method:** `PUT`
- **Path:** `/publicRestApiActions/editCampaign`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Pause or Resume Campaign](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign identifier to pause or resume. |
| `action` | body | `string` | yes | Use `pause` or `resume`. |
