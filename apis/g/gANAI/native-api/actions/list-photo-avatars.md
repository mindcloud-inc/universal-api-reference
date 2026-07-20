# List Photo Avatars with GAN.AI

Retrieves photo avatars from your GAN.AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/photo_avatars/list`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [List Photo Avatars](https://developer.gan.ai/api-reference/photo-avatars/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_datetime` | query | `string` | no |
| `start_datetime` | query | `string` | no |
| `status` | query | `string` | no |
| `title` | query | `string` | no |
