# Update Share Upload with HiDrive

Updates an existing share upload in HiDrive.

## Endpoint

- **Method:** `PUT`
- **Path:** `/shareupload`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Update Share Upload](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/shareupload_PUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Share upload ID to update. |
| `password` | body | `string` | no | Optional private share upload password. |
| `ttl` | body | `number` | no | Share upload expiry in seconds. |
| `maxcount` | body | `number` | no | Allowed upload count. |
| `maxsize` | body | `number` | no | Maximum upload file size in bytes. |
