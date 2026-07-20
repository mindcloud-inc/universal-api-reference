# Create Collection with pixx.io

Creates a new collection in your pixx.io workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/collections`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Create Collection](https://api.pixxio.com/docs/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional collection description. |
| `fileIDs` | body | `number<number>` | no | File IDs to include in a static collection. Send multiple values as a array. |
| `isDynamic` | body | `boolean` | no | Whether the collection is dynamic. |
| `name` | body | `string` | yes | The collection name. |
