# Create Comment Reply with Filestage

Creates a reply to a Filestage comment.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments/{commentId}/replies`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Create Comment Reply](https://developers.filestage.io/docs/api/u2y9vi6ddo0ul-create-comment-reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | Comment Id |
| `body` | body | `string` | yes | The body or comment contents. A user can be mentioned by fomarting in this manner `[~userId]`. Replace this `userId ` with the userId that was gotten from the `Get Mention Suggestions` API endpoint. |
| `teamOnly` | body | `boolean` | yes | — |
