# List Mail Uploads with HiDrive

Retrieves mail uploads from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/mailupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [List Mail Uploads](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/mailupload_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | no | Directory path for the mail upload. |
| `pid` | query | `string` | no | Directory public ID for the mail upload. |
