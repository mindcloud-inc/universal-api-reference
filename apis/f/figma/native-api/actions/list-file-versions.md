# List File Versions with Figma

Retrieves version history from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:key/versions`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Versions](https://developers.figma.com/docs/rest-api/version-history-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the file to list versions for. |
