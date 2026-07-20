# Publish entity to Prestashop with Wisewand

Publishes a Wisewand entity to Prestashop.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/publish/prestashop/:entity_id`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Publish entity to Prestashop](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | The ID of the entity to publish |
| `connection_id` | body | `string` | yes | The ID of the Prestashop connection to use |
