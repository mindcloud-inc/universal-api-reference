# Add Tags to Order with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [Add Tags to Order](https://shopify.dev/docs/api/admin-graphql/latest/mutations/tagsAdd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | — |
| `variables.id` | body | `string` | yes | Shopify Order GID, for example gid://shopify/Order/7151139979451. |
| `variables.tags[]` | body | `array<string>` | yes | One or more tags to add. Existing order tags are preserved. |
