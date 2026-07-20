# Delete Avatars with GAN.AI

Deletes avatars in bulk from GAN.AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/avatars/bulk_delete_avatars`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [Delete Avatars](https://developer.gan.ai/api-reference/avatars/bulk-delete-avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatarIds[]` | body | `array<string>` | yes | List of avatar IDs to delete. |
