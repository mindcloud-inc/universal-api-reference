# Get Template Sample Data with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/getSampleData`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Template Sample Data](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=58)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateName` | body | `string` | yes | The name of the template to inspect. |
| `format` | body | `string` | no | Response format for sample data. |
| `stringify` | body | `boolean` | no | Whether to stringify the JSON result. |
