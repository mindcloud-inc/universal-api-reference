# Upload File with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Upload File](https://developer.shipandco.com/en/#files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | File type: signature or logo. |
| `file` | body | `string` | yes | Base64-encoded PNG or JPEG file content, up to 1MB. |
