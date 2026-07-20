# Update Record with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/items/:itemId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Record](https://www.datocms.com/docs/content-management-api/resources/item/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | — |
| `data.attributes` | body | `object` | yes | — |
| `data.relationships` | body | `object` | no | Relationship links for the record payload. |
| `data.meta` | body | `object` | no | Record metadata block for status and workflow attributes. |
| `skip_item_validation` | query | `boolean` | no | Skip required validator checks while updating the record. |
| `skip_invalid` | query | `boolean` | no | Skip invalid records when processing update request. |
| `data.attributes.image.upload_id` | body | `string` | no | — |
| `data.attributes.image.alt` | body | `string` | no | — |
| `data.attributes.image.title` | body | `string` | no | — |
| `data.relationships.item_type.data` | body | `object` | no | — |
| `data.relationships.item_type.data.type` | body | `string` | no | — |
| `data.relationships.item_type.data.id` | body | `string` | no | — |
| `data.relationships.creator.data` | body | `object` | no | — |
| `data.attributes.category` | body | `string` | no | — |
| `data.attributes.content` | body | `string` | no | — |
| `data.attributes.image` | body | `object` | no | — |
| `data.attributes.title` | body | `string` | no | — |
| `data.meta.created_at` | body | `string` | no | — |
| `data.meta.current_version` | body | `string` | no | — |
| `data.meta.first_published_at` | body | `string` | no | — |
| `data.meta.has_children` | body | `boolean` | no | — |
| `data.meta.is_current_version_valid` | body | `boolean` | no | — |
| `data.meta.is_published_version_valid` | body | `boolean` | no | — |
| `data.meta.is_valid` | body | `boolean` | no | — |
| `data.meta.publication_scheduled_at` | body | `string` | no | — |
| `data.meta.published_at` | body | `string` | no | — |
| `data.meta.stage` | body | `string` | no | — |
| `data.meta.status` | body | `string` | no | — |
| `data.meta.unpublishing_scheduled_at` | body | `string` | no | — |
| `data.meta.updated_at` | body | `string` | no | — |
| `data.relationships.creator` | body | `object` | no | — |
| `data.relationships.item_type` | body | `object` | no | — |
