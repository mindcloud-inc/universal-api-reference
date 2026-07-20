# Get File Download URL with HiDrive

Retrieves a file download URL from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/file/url`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Get File Download URL](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/url_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | no | File path. |
| `pid` | query | `string` | no | File public ID. |
