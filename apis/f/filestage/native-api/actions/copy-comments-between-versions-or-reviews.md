# Copy Comments Between Versions or Reviews with Filestage

Copies comments between Filestage versions or reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/reviews/{reviewId}/comments/copy`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Copy Comments Between Versions or Reviews](https://developers.filestage.io/docs/api/28m6vxw2bt6tx-copy-comments-between-versions-or-reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | path | `string` | yes | The unique identifier of the **target** review where the comments will be copied to. |
| `sourceReviewId` | body | `string` | yes | The ID of the source review to copy the comments from. |
| `copyAll` | body | `boolean` | no | If `true`, all comments from the source are copied. If `false`, only the comments specified in the `commentIds` array are copied. |
| `commentIds[]` | body | `array<string>` | no | An array of specific comment IDs to copy from the source review. This is only used when `copyAll` is `false`. |
| `isBetweenVersions` | body | `boolean` | no | Determines the copy mode. If `true`, comments are copied from one version to another. If `false`, comments are copied from one review step to another. |
| `keepAnnotationsAndMarker` | body | `boolean` | no | If `true`, the comment's annotations and markers (positions on the file) are included in the copy. If `false`, only the comment text and metadata are copied. |
