# Rename Media Library with Sendible

## Endpoint

- **Method:** `PUT`
- **Path:** `0.1/tw/media_libraries`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Rename Media Library](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaLibraryId` | query | `string` | yes | The media library ID to rename. |
| `name` | body | `string` | yes | New media library name. |
