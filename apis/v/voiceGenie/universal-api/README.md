# <img src="https://images.mindcloud.co/apps/icons/voice-genie_1774904446856.png" alt="VoiceGenie logo" width="28" height="28"> VoiceGenie: Universal API

Manage voice agents, campaigns, and AI calling workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voiceGenie/latest
- **Category:** Support / Contact Center
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://voicegenie.ai
- **Vendor API docs:** https://voicegenie.gitbook.io/voicegenie-ai/integrations/public-api-integration

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Inbound Call Updates](actions/get-inbound-call-updates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Check Call Transfer Status](actions/check-call-transfer-status.md) | GET | Retrieves call transfer status from VoiceGenie. |
| [Get Call Analysis or Status](actions/get-call-analysis-or-status.md) | GET | Retrieves call analysis or status from VoiceGenie. |
| [Get Inbound Call Updates](actions/get-inbound-call-updates.md) | GET | Retrieves inbound call updates from VoiceGenie. |
| [Place a Call](actions/place-a-call.md) | POST | Creates a new call in VoiceGenie. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Pause or Resume Campaign](actions/pause-or-resume-campaign.md) | PUT | Updates a campaign's running state in VoiceGenie. |
| [Remove Customer from Campaign](actions/remove-customer-from-campaign.md) | PUT | Removes a customer from a VoiceGenie campaign. |

