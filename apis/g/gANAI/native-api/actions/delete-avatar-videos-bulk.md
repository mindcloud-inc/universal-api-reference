# Delete Avatar Videos Bulk with GAN.AI

Deletes avatar videos in bulk from GAN.AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/avatars/bulk_delete_avatar_inferences`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Delete Avatar Videos Bulk](https://developer.gan.ai/api-reference/avatars/bulk-delete-avatar-inferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inferenceIds[]` | body | `array<string>` | yes | List of avatar inference IDs to delete. |
