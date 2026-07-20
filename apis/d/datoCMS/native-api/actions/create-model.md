# Create Model with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/item-types`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Model](https://www.datocms.com/docs/content-management-api/resources/item-type/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | — |
| `data.attributes.api_key` | body | `string` | yes | — |
| `data.id` | body | `string` | no | Optional custom ID for the new model. |
| `data.attributes.singleton` | body | `boolean` | no | Set true when the model should allow only one record. |
| `data.attributes.all_locales_required` | body | `boolean` | no | Require all locales for localized fields. |
| `data.attributes.sortable` | body | `boolean` | no | Allow manual sorting of records. |
| `data.attributes.modular_block` | body | `boolean` | no | Create the model as a modular block model. |
| `data.attributes.inverse_relationships_enabled` | body | `boolean` | no | Enable inverse relationships on this model. |
| `data.attributes.draft_mode_active` | body | `boolean` | no | Enable draft mode for records in this model. |
| `data.attributes.draft_saving_active` | body | `boolean` | no | Enable partial draft-saving behavior. |
| `data.attributes.tree` | body | `boolean` | no | Enable tree/hierarchical records for this model. |
| `data.attributes.collection_appearance` | body | `string` | no | Collection appearance mode for the model. |
| `data.attributes.ordering_direction` | body | `string` | no | Default ordering direction for sorted collections. |
| `data.attributes.ordering_meta` | body | `string` | no | Ordering metadata configuration object. |
| `data.attributes.hint` | body | `string` | no | Optional hint shown to editors for this model. |
| `data.relationships.ordering_field.data.id` | body | `string` | no | Field ID used for default ordering. |
| `data.relationships.presentation_title_field.data.id` | body | `string` | no | Field ID used as presentation title. |
| `data.relationships.presentation_image_field.data.id` | body | `string` | no | Field ID used as presentation image. |
| `data.relationships.title_field.data.id` | body | `string` | no | Field ID used as model title field. |
| `data.relationships.image_preview_field.data.id` | body | `string` | no | Field ID used as image preview field. |
| `data.relationships.excerpt_field.data.id` | body | `string` | no | Field ID used as excerpt field. |
| `data.relationships.workflow.data.id` | body | `string` | no | Workflow ID associated with this model. |
| `skip_menu_item_creation` | query | `boolean` | no | Create the model without creating a menu item. |
| `menu_item_id` | query | `string` | no | Attach this model to an existing menu item. |
| `schema_menu_item_id` | query | `string` | no | Set the menu item under which this schema is created. |
| `data.attributes.ordering_meta.field` | body | `string` | no | — |
