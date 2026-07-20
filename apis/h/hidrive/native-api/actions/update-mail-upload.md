# Update Mail Upload with HiDrive

Updates an existing mail upload in HiDrive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/mailupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Update Mail Upload](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_PUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | yes | Mail upload path to update. |
| `pid` | body | `string` | no | Mail upload public ID to update. |
