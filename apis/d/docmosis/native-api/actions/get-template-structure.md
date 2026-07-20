# Get Template Structure with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/getTemplateStructure`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Template Structure](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=34)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateName` | body | `string` | yes | The name of the template to inspect. |
| `stringify` | body | `boolean` | no | Whether to stringify the JSON result. |
