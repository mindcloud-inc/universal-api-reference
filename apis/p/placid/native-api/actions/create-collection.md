# Create Collection with Placid

Creates a new collection in Placid.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/rest/collections`
- **Base URL:** `https://api.placid.app`
- **Official documentation:** [Create Collection](https://placid.app/docs/2.0/rest/collections#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title for the new collection. |
| `template_uuids[]` | body | `array<string>` | no | Template UUIDs to include in the collection. |
| `custom_data` | body | `object` | no | Custom data to store on the collection. |
