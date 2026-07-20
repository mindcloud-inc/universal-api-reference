# Create Product with Printify

Creates a product in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shop_id/products.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Create Product](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blueprint_id` | body | `number` | yes | Blueprint id to create from. |
| `description` | body | `string` | yes | Product description. |
| `print_areas` | body | `list<object>` | yes | Print area configuration with uploaded artwork. |
| `print_provider_id` | body | `number` | yes | Print provider id to create from. |
| `shop_id` | path | `number` | yes | Printify shop id. |
| `title` | body | `string` | yes | Product title. |
| `variants` | body | `list<object>` | yes | Enabled variants with prices. |
