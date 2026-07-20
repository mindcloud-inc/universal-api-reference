# Update Comment with Filestage

Updates a comment in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/{commentId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Comment](https://developers.filestage.io/docs/api/g7s1b9cvzldjh-update-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | — |
| `body` | body | `string` | yes | The body or comment contents. A user can be mentioned by fomarting in this manner `[~userId]`. Replace this `userId ` with the userId that was gotten from the `Get Mention Suggestions` API endpoint. |
| `teamOnly` | body | `boolean` | no | When `true`, comment is only visible to team members. |
