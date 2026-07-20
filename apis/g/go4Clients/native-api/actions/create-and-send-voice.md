# Create and Send Voice with Go4Clients

Creates a campaign and sends voice calls in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/voice/v2.0/event`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create and Send Voice](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationsList[]` | body | `array<string>` | yes | Destination phone numbers in international format. |
| `stepList[]` | body | `array<object>` | no | Step list for the IVR flow when not using a prebuilt IVR. |
| `ivrId` | body | `string` | no | Identifier for a prebuilt IVR. |
| `customFields` | body | `object` | no | Map of values used to personalize the IVR. |
| `sender` | body | `string` | yes | Caller ID shown to recipients. |
| `priority` | body | `string` | no | Priority of the calls in Go4Clients. |
| `scheduledDate` | body | `string` | no | Scheduled date in YYYY-MM-DDTHH:mm:sssZ format. |
| `campaignName` | body | `string` | yes | Campaign name to identify the call in analytics. |
| `text2speech` | body | `string` | no | Text that will be converted into voice for the call. |
| `voice` | body | `string` | no | Voice used to convert text to speech. |
