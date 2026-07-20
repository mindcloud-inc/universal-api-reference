# Create Share Link with HiDrive

Creates a new share link in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharelink`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Create Share Link](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | no | Optional private share link password. |
| `path` | body | `string` | no | File path for the share link. |
| `pid` | body | `string` | no | File public ID for the share link. |
| `ttl` | body | `number` | no | Share link expiry in seconds. |
| `maxcount` | body | `number` | no | Allowed successful downloads. |
