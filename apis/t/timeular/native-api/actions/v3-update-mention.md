# V3 Update Mention with Timeular

Updates an existing mention in the Timeular v3 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/mentions/:mentionId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Update Mention](https://developers.early.app/#b00ccf63-701c-471f-abd1-31735f6224d3)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | body | `string` | no |
| `mentionId` | path | `string` | yes |
