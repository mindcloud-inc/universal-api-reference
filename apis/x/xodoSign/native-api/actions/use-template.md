# Use Template with Xodo Sign

Creates a new document from a template in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Use Template](https://eversign.com/api/documentation/methods#use-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the template. |
| `sandbox` | body | `string` | no | Set to 1 to enable sandbox mode for document creation from a template. |
| `title` | body | `string` | no | Title for the document created from the template. |
| `template_id` | body | `string` | yes | The template hash to instantiate as a document. |
