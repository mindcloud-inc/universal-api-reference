# Place a Call with VoiceGenie

Creates a new call in VoiceGenie.

## Endpoint

- **Method:** `POST`
- **Path:** `/publicRestApiActions/placeCall`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Place a Call](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Recurring campaign ID that should receive the call. |
| `customerNumber` | body | `string` | yes | Customer number in E.164 format with a leading + and no spaces or punctuation. |
| `customerInformation` | body | `object` | no | Optional object of string values used for dynamic variables such as first_name and last_name. |
