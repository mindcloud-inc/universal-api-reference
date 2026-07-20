# Publish entity to WordPress with Wisewand

Publishes a Wisewand entity to WordPress.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/publish/wordpress/:entity_id`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Publish entity to WordPress](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | The ID of the entity to publish |
| `connection_id` | body | `string` | yes | The ID of the WordPress connection to use |
| `status` | body | `string` | yes | The status of the post |
