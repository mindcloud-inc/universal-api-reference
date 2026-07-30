# Convert PNG to PDF with ConvertAPI

Converts a PNG file to PDF with ConvertAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/convert/png/to/pdf`
- **Base URL:** `https://v2.convertapi.com`
- **Official documentation:** [Convert PNG to PDF](https://www.convertapi.com/jpg-to-pdf)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parameters[].FileValue.Name` | body | `string` | no | The current name of the file. |
| `parameters[].Name` | body | `string` | no | — |
| `storeFile` | body | `boolean` | no | When the `StoreFile` parameter is set to `True`, your converted file is written to ConvertAPI’s encrypted, temporary storage and made available via a time-limited secure download URL, valid for up to 3 hours. After this period, the file is permanently deleted. When `StoreFile` is set to `False`, conversion happens entirely in-memory. The raw file bytes are streamed back in the API response without touching disk or external storage, ensuring maximum security and zero persistence so that only you can access the content. |
| `parameters[].FileValue` | body | `object` | no | — |
| `parameters[].FileValue.Data` | body | `string` | no | A base64 encoded string of your png image - or an image url. |
| `pdfa` | body | `boolean` | no | Create PDF/A-1b compliant document. |
| `parameters[]` | body | `array<object>` | no | — |
