# Create Share Upload with HiDrive

Creates a new share upload in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/shareupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Create Share Upload](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | no | Optional private share upload password. |
| `path` | body | `string` | no | Directory path for the share upload. |
| `pid` | body | `string` | no | Directory public ID for the share upload. |
| `ttl` | body | `number` | no | Share upload expiry in seconds. |
| `maxcount` | body | `number` | no | Allowed upload count. |
| `maxsize` | body | `number` | no | Maximum upload file size in bytes. |
