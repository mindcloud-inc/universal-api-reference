# Delete Image with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteImage`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Delete Image](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=51)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageName[]` | body | `array<string>` | yes | Image name or names to delete, as documented by Docmosis. |
