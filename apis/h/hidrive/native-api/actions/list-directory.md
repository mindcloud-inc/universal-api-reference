# List Directory with HiDrive

Retrieves a directory from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/dir`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [List Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_GET)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated directory fields to include. |
| `members` | query | `string` | no | Directory member types to include, such as all. |
| `path` | query | `string` | no | Path to the directory. |
| `pid` | query | `string` | no | HiDrive public ID for the directory. |
| `sort` | query | `string` | no | Sort by name, category, mtime, type, or size. Prefix with - for descending. |
| `limit` | query | `number` | no | Maximum number of directory entries to return. |
