# Render Template Version with HTML/CSS to Image app

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/image/:templateId/:templateVersion`
- **Base URL:** `https://hcti.io`
- **Official documentation:** [Render Template Version](https://docs.htmlcsstoimage.com/getting-started/templates/#creating-an-image-with-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Identifier of the template to render. |
| `templateVersion` | path | `number` | yes | Specific template version to render. |
| `template_values` | body | `object` | yes | Object of values to substitute into the template. |
