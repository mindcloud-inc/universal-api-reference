# Add Calls to Voice Campaign with Go4Clients

Adds calls to an existing Go4Clients voice campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/voice/v1.0/{{voice_campaign_id}}`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Add Calls to Voice Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_campaign_id` | path | `string` | yes | Voice campaign identifier. |
| `destinationsList[]` | body | `array<string>` | yes | Destination list of phone numbers. |
| `stepList[]` | body | `array<object>` | no | IVR step list when not using a prebuilt IVR. |
| `ivrId` | body | `string` | no | Identifier for a prebuilt IVR. |
| `customFields` | body | `object` | no | Map of personalized IVR fields. |
| `priority` | body | `string` | no | Priority of the voice calls. |
| `scheduledDate` | body | `string` | no | Scheduled date in YYYY-MM-DDTHH:mm:sssZ format. |
