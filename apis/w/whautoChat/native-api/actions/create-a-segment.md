# Create a Segment with WhautoChat

Creates a new segment in WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/segments`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Create a Segment](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/segment/#2-create-a-segment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `type` | body | `string` | no |
| `status` | body | `string` | no |
| `segments[]` | body | `array<object>` | no |
| `retargetBroadcast.id` | body | `string` | no |
| `retargetEngagementType` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
| `startedAt` | body | `string` | no |
| `completedAt` | body | `string` | no |
