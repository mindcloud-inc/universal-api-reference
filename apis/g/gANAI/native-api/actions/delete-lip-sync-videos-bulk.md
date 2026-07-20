# Delete LipSync Videos Bulk with GAN.AI

Deletes lip-sync videos in bulk from GAN.AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/lipsync/bulk_delete_lipsyncs`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Delete LipSync Videos Bulk](https://developer.gan.ai/api-reference/lipsync/bulk-delete-lipsyncs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inferenceIds[]` | body | `array<string>` | yes | List of Lip Sync inference IDs to delete. |
