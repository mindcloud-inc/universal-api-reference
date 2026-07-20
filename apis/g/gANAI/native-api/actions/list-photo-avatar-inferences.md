# List Photo Avatar Inferences with GAN.AI

Retrieves photo avatar inferences from your GAN.AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/photo_avatars/list_inference`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [List Photo Avatar Inferences](https://developer.gan.ai/api-reference/photo-avatars/list-inference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_datetime` | query | `string` | no |
| `photo_avatar_id` | query | `string` | no |
| `start_datetime` | query | `string` | no |
| `status` | query | `string` | no |
| `title` | query | `string` | no |
