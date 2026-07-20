# Update Reviewer Group Settings with Filestage

Updates settings for a Filestage reviewer group.

## Endpoint

- **Method:** `PUT`
- **Path:** `/steps/{stepId}/settings`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Reviewer Group Settings](https://developers.filestage.io/docs/api/hjfk7udk1cx3k-update-reviewer-group-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | path | `string` | yes | — |
| `downloadInReview` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file status is `In Review`. |
| `downloadNeedsChanges` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file has been marked as `Need Changes`. |
| `downloadApproved` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file has been approved. |
| `commentInReview` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `In review`. |
| `commentNeedsChanges` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `Needs Changes` |
| `commentApproved` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the file has been approved. |
| `emailNotifications` | body | `boolean` | no | If you this setting is set as false, reviewers without a registered account will no longer receive email notifications for project activities (new comments, new files and versions, file status changes and submitted reviews). |
| `passwordProtection` | body | `boolean` | no | When this setting is true, any new reviewers without a Filestage account will need to enter the password as specified in the `password` field |
| `uploadingEnabled` | body | `boolean` | no | If this setting is set as `true`, external reviewers will be able to upload new files and new versions to this reviewer group. |
| `anonymousReviewers` | body | `boolean` | no | If you this setting as `true`, all reviewers will be anonymous to each other. |
| `password` | body | `string` | no | This field is required when `passwordProtection` is set as `true`. It creates a password to protect this reviewer group. |
