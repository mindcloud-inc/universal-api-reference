# VoiceGenie: Native API Reference

A consolidated summary of VoiceGenie's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration
- **API base URL:** `https://core-saas.voicegenie.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · VoiceGenie workspace ID generated for your account.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Call Transfer Status](actions/check-call-transfer-status.md) | `POST /publicRestApiActions/checkCallTransferStatus` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
| [Get Call Analysis or Status](actions/get-call-analysis-or-status.md) | `POST /publicRestApiActions/callAnalysisOrStatus` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
| [Get Inbound Call Updates](actions/get-inbound-call-updates.md) | `POST /publicRestApiActions/inboundCallUpdate` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
| [Pause or Resume Campaign](actions/pause-or-resume-campaign.md) | `PUT /publicRestApiActions/editCampaign` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
| [Place a Call](actions/place-a-call.md) | `POST /publicRestApiActions/placeCall` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
| [Remove Customer from Campaign](actions/remove-customer-from-campaign.md) | `PUT /publicRestApiActions/pullCustomerFromCampaign` | [docs](https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration) |
