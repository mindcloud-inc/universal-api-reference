# Pin or Unpin a Comment with Filestage

Pins or unpins a comment in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/{commentId}/pinned`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Pin or Unpin a Comment](https://developers.filestage.io/docs/api/u4tj3rcpol3g0-pin-or-unpin-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | — |
| `isPinned` | body | `boolean` | no | When the value is `true` the comment is pinned and when the value is `false`, the comment is unpinned. |
