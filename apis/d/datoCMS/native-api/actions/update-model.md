# Update Model with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/item-types/:itemTypeId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Model](https://www.datocms.com/docs/content-management-api/resources/item-type/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemTypeId` | path | `string` | yes | Model ID or API key. |
| `data.attributes` | body | `object` | yes | Model attributes payload. |
| `data.attributes.name` | body | `string` | no | — |
| `data.attributes.api_key` | body | `string` | no | — |
| `data.attributes.collection_appeareance` | body | `string` | no | — |
| `data.attributes.collection_appearance` | body | `string` | no | — |
| `data.attributes.singleton` | body | `boolean` | no | — |
| `data.attributes.all_locales_required` | body | `boolean` | no | — |
| `data.attributes.sortable` | body | `boolean` | no | — |
| `data.attributes.modular_block` | body | `boolean` | no | — |
| `data.attributes.draft_mode_active` | body | `boolean` | no | — |
| `data.attributes.draft_saving_active` | body | `boolean` | no | — |
| `data.attributes.tree` | body | `boolean` | no | — |
| `data.attributes.ordering_direction` | body | `string` | no | — |
| `data.attributes.ordering_meta` | body | `string` | no | — |
| `data.attributes.has_singleton_item` | body | `boolean` | no | — |
| `data.attributes.hint` | body | `string` | no | — |
| `data.attributes.inverse_relationships_enabled` | body | `boolean` | no | — |
