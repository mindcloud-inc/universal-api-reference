# Delete Campaign Tag with Pitchbox

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/campaigns/:campaignId/tags/:tagId`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [Delete Campaign Tag](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The campaign id. |
| `tagId` | path | `number` | yes | The id of the tag to remove from the campaign. |
