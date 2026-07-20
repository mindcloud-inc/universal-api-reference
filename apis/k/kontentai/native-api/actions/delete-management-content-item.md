# Delete management content item with Kontent.ai

Deletes a content item from Kontent.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Delete management content item](https://kontent.ai/learn/docs/apis/management-api-v2/content-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_identifier` | path | `string` | yes | Kontent.ai content item identifier to delete. |
