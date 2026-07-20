# Add Reviewer Group to Project Template with Filestage

Creates a reviewer group in a Filestage project template.

## Endpoint

- **Method:** `POST`
- **Path:** `/project-templates/{projectTemplateId}/steps`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add Reviewer Group to Project Template](https://developers.filestage.io/docs/api/a4xce2oplgd79-add-reviewer-group-to-project-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectTemplateId` | path | `string` | yes | ID of the project template |
| `name` | body | `string` | yes | The name of the reviewer group. |
| `settings.downloadInReview` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file status is `In Review`. |
| `settings.downloadNeedsChanges` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file has been marked as `Need Changes`. |
| `settings.downloadApproved` | body | `boolean` | no | If you this setting is false, the download button won't be visible for reviewers file has been approved. |
| `settings.commentInReview` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `In review`. |
| `settings.commentNeedsChanges` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `Needs Changes` |
| `settings.commentApproved` | body | `boolean` | no | If you this is set as false, reviewers cannot create, edit or delete comments when the file has been approved. |
| `settings.emailNotifications` | body | `boolean` | no | If you this setting is set as false, reviewers without a registered account will no longer receive email notifications for project activities (new comments, new files and versions, file status changes and submitted reviews). |
| `settings.passwordProtection` | body | `boolean` | no | When this setting is true, any new reviewers without a Filestage account will need to enter the password as specified in the `password` field |
| `settings.uploadingEnabled` | body | `boolean` | no | If this setting is set as `true`, external reviewers will be able to upload new files and new versions to this reviewer group. |
| `settings.anonymousReviewers` | body | `boolean` | no | If you this setting as `true`, all reviewers will be anonymous to each other. |
| `settings.password` | body | `string` | no | This field is required when `passwordProtection` is set as `true`. It creates a password to protect this reviewer group. |
