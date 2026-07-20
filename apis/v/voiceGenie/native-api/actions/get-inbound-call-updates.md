# Get Inbound Call Updates with VoiceGenie

Retrieves inbound call updates from VoiceGenie.

## Endpoint

- **Method:** `POST`
- **Path:** `/publicRestApiActions/inboundCallUpdate`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Get Inbound Call Updates](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign tied to the inbound number. |
