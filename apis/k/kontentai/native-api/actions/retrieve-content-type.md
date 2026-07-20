# Retrieve content type with Kontent.ai

Retrieves a content type from Kontent.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/types/:type_codename`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Retrieve content type](https://kontent.ai/learn/docs/apis/delivery-api/content-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `type_codename` | path | `string` | yes | Content type codename. |
