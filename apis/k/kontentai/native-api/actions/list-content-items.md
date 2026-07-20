# List content items with Kontent.ai

Retrieves content items from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/items`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [List content items](https://kontent.ai/learn/docs/apis/delivery-api/content-items)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `language` | query | `string` | no | Language codename used to localize returned content. |
| `depth` | query | `number` | no | How many levels of linked content to include. |
| `elements` | query | `string` | no | Comma-separated element codenames to include. Send multiple values as a string separated by `,`. |
| `excludeElements` | query | `string` | no | Comma-separated element codenames to exclude. Send multiple values as a string separated by `,`. |
| `system.type` | query | `string` | no | Filter content items by content type codename. |
