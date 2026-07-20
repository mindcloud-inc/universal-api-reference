# List User LipSyncs with GAN.AI

Retrieves lip-sync videos from your GAN.AI account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/lipsync/get_user_lipsyncs`
- **Base URL:** `https://os.gan.ai`
- **Official documentation:** [List User LipSyncs](https://developer.gan.ai/api-reference/lipsync/get-user-lipsyncs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_datetime` | query | `string` | no |
| `start_datetime` | query | `string` | no |
| `status` | query | `string` | no |
| `title` | query | `string` | no |
