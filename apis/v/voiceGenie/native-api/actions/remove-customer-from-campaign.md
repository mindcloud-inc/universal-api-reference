# Remove Customer from Campaign with VoiceGenie

Removes a customer from a VoiceGenie campaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/publicRestApiActions/pullCustomerFromCampaign`
- **Base URL:** `https://core-saas.voicegenie.ai/api/v1`
- **Official documentation:** [Remove Customer from Campaign](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | Campaign identifier to update. |
| `customerNumber` | body | `string` | yes | Customer number in E.164 format with a leading + and no spaces or punctuation. |
