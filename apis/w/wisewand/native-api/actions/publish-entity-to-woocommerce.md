# Publish entity to WooCommerce with Wisewand

Publishes a Wisewand entity to WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/publish/woocommerce/:entity_id`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Publish entity to WooCommerce](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | The ID of the entity to publish |
| `connection_id` | body | `string` | yes | The ID of the WooCommerce connection to use |
