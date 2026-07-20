# Create Review Comment with Filestage

Creates a review comment in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/reviews/{reviewId}/comments`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Create Review Comment](https://developers.filestage.io/docs/api/3rj5isxwlfnwu-create-review-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | path | `string` | yes | Review Id |
| `body` | body | `string` | yes | The body or comment contents. A user can be mentioned by formatting in this manner `[~userId]`. Replace this `userId ` with the userId that was gotten from the `Get Mention Suggestions` API endpoint. |
| `teamOnly` | body | `boolean` | yes | — |
| `attachmentFileURLs[]` | body | `array<string>` | no | This is an array of file urls to be attached when creating a comment for a review. |
| `marker` | body | `object` | no | The Marker is an object that describe the position of a user comment on the file |
