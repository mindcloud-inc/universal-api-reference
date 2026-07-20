# Create External Share with pixx.io

Creates a new external share in your pixx.io workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/externalShares`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Create External Share](https://api.pixxio.com/docs/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionID` | body | `number` | no | Collection ID to share. |
| `fileIDs` | body | `number<number>` | no | File IDs to share. Send multiple values as a array. |
| `name` | body | `string` | yes | The external share name. |
| `validityPeriod` | body | `string` | no | The duration until the share link expires. |
