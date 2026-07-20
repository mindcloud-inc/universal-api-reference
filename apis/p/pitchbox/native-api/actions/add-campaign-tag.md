# Add Campaign Tag with Pitchbox

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/:campaignId/tags`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [Add Campaign Tag](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | The campaign id. |
| `tag` | body | `number` | yes | The id of the tag to attach to the campaign. |
