# Add Prospect Tag with ManyReach

Adds a tag to a prospect in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/prospects/:id/tags`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Add Prospect Tag](https://api.manyreach.com/api#v2/tag/prospect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Prospect ID. |
| `tagId` | body | `string` | yes | Tag ID to attach to the prospect. |
