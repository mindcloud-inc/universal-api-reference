# Update Share Link with HiDrive

Updates an existing share link in HiDrive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sharelink`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Update Share Link](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/sharelink_PUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Share link ID to update. |
| `password` | body | `string` | no | Optional private share link password. |
| `ttl` | body | `number` | no | Share link expiry in seconds. |
| `maxcount` | body | `number` | no | Allowed successful downloads. |
