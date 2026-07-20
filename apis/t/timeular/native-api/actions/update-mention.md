# Update Mention with Timeular

Updates an existing mention in your Timeular workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/mentions/:mentionId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Mention](https://developers.early.app/#e0d26363-ad2a-493c-a118-7f61e270e7ee)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | body | `string` | no |
| `mentionId` | path | `string` | yes |
