# Update Comment Resolution with Filestage

Updates the resolution status of a Filestage comment.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/{commentId}/resolution`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Comment Resolution](https://developers.filestage.io/docs/api/pmjv5qalq096u-update-comment-resolution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | — |
| `resolved` | body | `boolean` | no | When the value is `true` the comment is marked as complete and when the value is `false`, the comment is incomplete. |
