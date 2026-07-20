# List Template Layers with Templated

Retrieves layers for a template in Templated.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/template/:id/layers`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [List Template Layers](https://templated.io/docs/templates/layers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The template id of the template that you want to retrieve the layers. |
| `includeLockedLayers` | query | `boolean` | no | When true, return layers marked as locked in the template. |
