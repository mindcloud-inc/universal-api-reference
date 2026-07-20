# Update Collection with Placid

Updates an existing collection in Placid.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/rest/collections/:collectionId`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Update Collection](https://placid.app/docs/2.0/rest/collections#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | ID of the collection to update. |
| `title` | body | `string` | no | Updated title for the collection. |
| `template_uuids[]` | body | `array<string>` | no | Full list of template UUIDs that should remain in the collection. |
| `add_template_uuids[]` | body | `array<string>` | no | Template UUIDs to add to the collection. |
| `remove_template_uuids[]` | body | `array<string>` | no | Template UUIDs to remove from the collection. |
| `custom_data` | body | `object` | no | Updated custom data for the collection. |
