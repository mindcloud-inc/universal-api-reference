# Get File Hashes with HiDrive

Retrieves file hashes from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/file/hash`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Get File Hashes](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/hash_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | no | File path. |
| `pid` | query | `string` | no | File public ID. |
| `level` | query | `number` | yes | Hash level requested. |
| `ranges` | query | `string` | yes | Comma-separated byte ranges. |
