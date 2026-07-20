# Get Image with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/getImage`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Image](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=52)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageName[]` | body | `array<string>` | yes | Image name or names to download, as documented by Docmosis. |
