# List Media with Postpone

Retrieves media from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [List Media](https://developers.postpone.app/examples/example-queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.orderBy` | body | `string` | no | Sort order such as -date_created. |
| `variables.limit` | body | `number` | no | Maximum number of media files to return. |
| `variables.page` | body | `number` | no | Page number for pagination. |
| `variables.search` | body | `string` | no | Search term for media filenames. |
| `variables.fileType` | body | `string` | no | Optional file type such as IMAGE, VIDEO, GIF, or AUDIO. |
