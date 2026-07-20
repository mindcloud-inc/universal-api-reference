# Create Collection with Bannerbear

Creates a new collection in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/collections`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Collection](https://developers.bannerbear.com/v2/#collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_set` | body | `string` | yes | The template set uid that you want to use. |
| `modifications[]` | body | `array<object>` | yes | A list of modifications you want to make. |
| `modifications[].name` | body | `string` | yes | The name of the layer you want to change. |
| `modifications[].text` | body | `string` | no | Replacement text you want to use. |
| `modifications[].image_url` | body | `string` | no | URL to an image file. |
| `modifications[].color` | body | `string` | no | Color in hex format, for example #FF0000. |
| `modifications[].background` | body | `string` | no | Background color in hex format, for example #FF0000. |
| `webhook_url` | body | `string` | no | A URL to POST the full Collection object to upon rendering completion. |
| `metadata` | body | `string` | no | Any metadata that you need to store, for example a record ID. |
| `transparent` | body | `boolean` | no | Render the collection with a transparent background. |
