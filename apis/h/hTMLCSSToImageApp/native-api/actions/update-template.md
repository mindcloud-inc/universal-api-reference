# Update Template with HTML/CSS to Image app

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/template/:templateId`
- **Base URL:** `https://hcti.io`
- **Official documentation:** [Update Template](https://docs.htmlcsstoimage.com/getting-started/templates/#editing-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | Identifier of the template to update. |
| `html` | body | `string` | yes | Updated HTML markup for the template. |
| `css` | body | `string` | no | Updated CSS styles for the template. |
| `name` | body | `string` | no | Updated template name. |
| `description` | body | `string` | no | Updated template description. |
