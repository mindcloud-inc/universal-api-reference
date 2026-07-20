# List Avatars with GAN.AI

Retrieves avatars from your GAN.AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/avatars/list`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [List Avatars](https://developer.gan.ai/api-reference/avatars/get-avatar-list-for-user)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_datetime` | query | `string` | no |
| `start_datetime` | query | `string` | no |
| `status` | query | `string` | no |
| `title` | query | `string` | no |
