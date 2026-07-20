# Upsert management content item with Kontent.ai

Upserts a content item in Kontent.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Upsert management content item](https://kontent.ai/learn/docs/apis/management-api-v2/content-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_identifier` | path | `string` | yes | Kontent.ai content item identifier to upsert. |
| `body` | body | `object` | yes | JSON request body for upserting a Kontent.ai management content item. |
