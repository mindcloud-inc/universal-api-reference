# Detach Attachment from Object with Asset Panda

Detaches an attachment from an object in Asset Panda.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/groups/:groupId/objects/:groupObjectId/attachment/:attachmentId/detach`
- **Base URL:** `https://api.assetpanda.com`
- **Official documentation:** [Detach Attachment from Object](https://team-asset-panda.readme.io/reference/put_v3-groups-group-id-objects-group-object-id-attachment-attachment-id-detach)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attachment_id` | path | `string` | no |
| `group_id` | path | `string` | no |
| `group_object_id` | path | `string` | no |
