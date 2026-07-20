# V3 Update Tag with Timeular

Updates an existing tag in the Timeular v3 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/tags/:tagId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Update Tag](https://developers.early.app/#34edd1e9-c5fd-47f3-83a6-bc16e6409d11)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `label` | body | `string` | no |
| `tagId` | path | `string` | yes |
