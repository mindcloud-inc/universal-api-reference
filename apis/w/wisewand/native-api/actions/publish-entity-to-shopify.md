# Publish entity to Shopify with Wisewand

Publishes a Wisewand entity to Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/publish/shopify/:entity_id`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Publish entity to Shopify](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | The ID of the entity to publish |
| `connection_id` | body | `string` | yes | The ID of the Shopify connection to use |
