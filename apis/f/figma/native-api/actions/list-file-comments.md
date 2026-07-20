# List File Comments with Figma

Retrieves comments from a Figma file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:key/comments`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List File Comments](https://developers.figma.com/docs/rest-api/comments-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Key of the Figma file. |
| `as_md` | query | `boolean` | no | When true, return comments as Markdown text. |
