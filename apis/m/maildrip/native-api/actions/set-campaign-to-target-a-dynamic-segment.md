# Set campaign to target a dynamic segment with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaignId}/segment`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Set campaign to target a dynamic segment](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign |
| `segmentId` | body | `string` | no | ID of the segment to target |
