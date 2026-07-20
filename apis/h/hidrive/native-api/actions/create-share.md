# Create Share with HiDrive

Creates a new share in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/share`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Create Share](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `password` | body | `string` | no | Optional share password. |
| `path` | body | `string` | no | Directory path to share. |
| `pid` | body | `string` | no | Directory public ID to share. |
| `ttl` | body | `number` | no | Share expiry in seconds. |
| `maxcount` | body | `number` | no | Maximum issued share tokens. |
| `writable` | body | `boolean` | no | Allow write access to the shared folder. |
