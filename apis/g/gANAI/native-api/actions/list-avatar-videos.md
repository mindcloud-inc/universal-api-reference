# List Avatar Videos with GAN.AI

Retrieves avatar videos from your GAN.AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/avatars/list_inferences`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [List Avatar Videos](https://developer.gan.ai/api-reference/avatars/avatar-inferences-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `avatar_id` | query | `string` | no |
| `avatar_title` | query | `string` | no |
| `end_datetime` | query | `string` | no |
| `inference_title` | query | `string` | no |
| `start_datetime` | query | `string` | no |
| `status` | query | `string` | no |
