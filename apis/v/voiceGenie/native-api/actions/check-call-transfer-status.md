# Check Call Transfer Status with VoiceGenie

Retrieves call transfer status from VoiceGenie.

## Endpoint

- **Method:** `POST`
- **Path:** `/publicRestApiActions/checkCallTransferStatus`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Check Call Transfer Status](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign associated with the transfer. |
