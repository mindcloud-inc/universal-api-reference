# Add Personalized IVR with Go4Clients

Adds a personalized IVR to a Go4Clients voice campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/voice/v1.0/{{voice_campaign_id}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Add Personalized IVR](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_campaign_id` | path | `string` | yes | Voice campaign identifier. |
| `destinationsList[]` | body | `array<string>` | yes | Destination list of phone numbers. |
| `ivrId` | body | `string` | no | Identifier of the IVR to use in the call. |
| `customFields` | body | `object` | no | Map of values used to personalize the IVR. |
| `stepList[]` | body | `array<object>` | no | Optional IVR step list when no IVR ID is provided. |
