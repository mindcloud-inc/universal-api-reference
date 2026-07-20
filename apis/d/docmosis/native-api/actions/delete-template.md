# Delete Template with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteTemplate`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Delete Template](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=39)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateName[]` | body | `array<string>` | yes | One or more template names to delete. |
