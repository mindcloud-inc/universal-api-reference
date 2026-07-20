# Rename Tag with Inoreader

Renames an existing tag in Inoreader.

## Endpoint

- **Method:** `POST`
- **Path:** `/rename-tag`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Rename Tag](https://www.inoreader.com/developers/rename-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | body | `string` | yes | Full source tag or folder name, for example user/-/label/Tech. |
| `dest` | body | `string` | yes | New tag or folder name without forward slashes. |
