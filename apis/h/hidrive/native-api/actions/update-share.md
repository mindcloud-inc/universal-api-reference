# Update Share with HiDrive

Updates an existing share in HiDrive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/share`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Update Share](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/share_PUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Share ID to update. |
| `password` | body | `string` | no | Optional share password. |
| `ttl` | body | `number` | no | Share expiry in seconds. |
| `maxcount` | body | `number` | no | Maximum issued share tokens. |
| `writable` | body | `boolean` | no | Allow write access to the shared folder. |
