# Get Call Analysis or Status with VoiceGenie

Retrieves call analysis or status from VoiceGenie.

## Endpoint

- **Method:** `POST`
- **Path:** `/publicRestApiActions/callAnalysisOrStatus`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Get Call Analysis or Status](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign associated with the call. |
| `customerNumber` | body | `string` | yes | Customer number used in the campaign, preferably in E.164 format. |
| `action` | body | `string` | yes | Use `analysis` for transcripts or `status` for the latest call state. |
