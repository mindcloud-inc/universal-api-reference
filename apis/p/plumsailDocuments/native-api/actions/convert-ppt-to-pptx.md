# Convert PPT to PPTX with Plumsail Documents

Converts PPT to PPTX in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/ppt-to-pptx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert PPT to PPTX](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `File` | body | `file` | no | PPT file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a PPT file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
