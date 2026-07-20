# Retrieve content item with Kontent.ai

Retrieves a content item from Kontent.ai by codename.

## Endpoint

- **Method:** `GET`
- **Path:** `/:environment_id/items/:item_codename`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Retrieve content item](https://kontent.ai/learn/docs/apis/delivery-api/content-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Kontent.ai project environment identifier. |
| `item_codename` | path | `string` | yes | Content item codename. |
| `language` | query | `string` | no | Language codename used to localize returned content. |
| `depth` | query | `number` | no | How many levels of linked content to include. |
| `elements` | query | `string` | no | Comma-separated element codenames to include. Send multiple values as a string separated by `,`. |
| `excludeElements` | query | `string` | no | Comma-separated element codenames to exclude. Send multiple values as a string separated by `,`. |
