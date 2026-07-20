# Remove Prospect Tag with ManyReach

Deletes a tag from a prospect in ManyReach.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://api.manyreach.com/api/v2/prospects/:id/tags/:tagId`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Remove Prospect Tag](https://api.manyreach.com/api#v2/tag/prospect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Prospect ID. |
| `tagId` | path | `string` | no | Tag ID. |
