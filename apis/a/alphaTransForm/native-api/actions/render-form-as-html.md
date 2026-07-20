# Render Form As HTML with Alpha TransForm

Retrieves rendered HTML for form data in Alpha TransForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/RenderFormAsHTML`
- **Base URL:** `https://transform.alphasoftware.com/transformAPIVersion1.a5svc`
- **Official documentation:** [Render Form As HTML](https://documentation.alphasoftware.com/TransFormDocumentation/pages/Ref/API/RenderFormAsHTML.xml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formInstanceid` | body | `string` | no | The formInstanceId of the form data you wish to render as HTML |
| `formName` | body | `string` | no | The form id of the form you want to use as the template for the HTML. If you do not specify a value the same form definition as was used to collect the data is used. |
