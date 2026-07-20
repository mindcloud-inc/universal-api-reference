# Download Template with Carbone.io

Downloads a template from Carbone.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/[:templateId-or-versionId]`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [Download Template](https://carbone.io/documentation/developer/http-api/manage-templates.html#download-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId-or-versionId` | path | `string` | yes | Template ID (64-bit) or Version ID (SHA-256) to download. |
