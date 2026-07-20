# <img src="https://images.mindcloud.co/apps/icons/filestage_1774469900442.png" alt="Filestage logo" width="28" height="28"> Filestage: Universal API

Review and approval workspace for managing Filestage projects, files, reviewer groups, reviews, and comments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/filestage/latest
- **Category:** Content & Files / Storage
- **Actions:** 81
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://filestage.io
- **Vendor API docs:** https://developers.filestage.io/docs/api/a3dwkuuqd37h7-welcome-to-our-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (81)

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [Remove Collaborator](actions/remove-collaborator.md) | DELETE | Deletes a collaborator from a Filestage project. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Copy Comments Between Versions or Reviews](actions/copy-comments-between-versions-or-reviews.md) | POST | Copies comments between Filestage versions or reviews. |
| [Create Comment Reply](actions/create-comment-reply.md) | POST | Creates a reply to a Filestage comment. |
| [Create Review Comment](actions/create-review-comment.md) | POST | Creates a review comment in Filestage. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Filestage by ID. |
| [List Comments by Review](actions/list-comments-by-review.md) | GET | Retrieves comments from a Filestage review. |
| [Pin or Unpin a Comment](actions/pin-or-unpin-a-comment.md) | PUT | Pins or unpins a comment in Filestage. |
| [Remove Comment](actions/remove-comment.md) | DELETE | Deletes a comment from Filestage. |
| [Update Comment](actions/update-comment.md) | PUT | Updates a comment in Filestage. |
| [Update Comment Resolution](actions/update-comment-resolution.md) | PUT | Updates the resolution status of a Filestage comment. |

### Comment Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Comment Attachment](actions/download-comment-attachment.md) | GET | Downloads a Filestage comment attachment. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File by ID](actions/get-file-by-id.md) | GET | Retrieves a file from Filestage by ID. |
| [Import Website](actions/import-website.md) | POST | Creates a website file in Filestage from a URL. |
| [List Files by Parameters](actions/list-files-by-parameters.md) | GET | Finds Filestage files by external ID or form answer. |
| [List Files by Project](actions/list-files-by-project.md) | GET | Retrieves files from a Filestage project. |
| [List Files in Section](actions/list-files-in-section.md) | GET | Retrieves files from a Filestage section. |
| [Move File to a Section](actions/move-file-to-a-section.md) | PUT | Moves a Filestage file to a section. |
| [Remove File](actions/remove-file.md) | DELETE | Deletes a file from Filestage by ID. |
| [Remove File by External ID](actions/remove-file-by-external-id.md) | DELETE | Deletes a Filestage file by external ID. |
| [Upload File](actions/upload-file.md) | POST | Creates a new file in Filestage from a URL. |

### File Upload

| Action | Method | Description |
| --- | --- | --- |
| [Generate Presigned Upload URL](actions/generate-presigned-upload-url.md) | POST | Creates a presigned upload URL in Filestage. |

### File Version

| Action | Method | Description |
| --- | --- | --- |
| [Download File Version](actions/download-file-version.md) | GET | Downloads a file version from Filestage. |
| [Get File URL](actions/get-file-url.md) | GET | Retrieves a file URL from Filestage by version. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Filestage. |
| [Get Folder by ID](actions/get-folder-by-id.md) | GET | Retrieves a folder from Filestage by ID. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Filestage. |

### Mention Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [List Mention Suggestions](actions/list-mention-suggestions.md) | GET | Retrieves mention suggestions from Filestage. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Collaborators to Project](actions/add-collaborators-to-project.md) | POST | Adds collaborators to a Filestage project. |
| [Archive or Unarchive Project by ID](actions/archive-or-unarchive-project-by-id.md) | PUT | Archives or unarchives a Filestage project by ID. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Filestage. |
| [Get Project by ID](actions/get-project-by-id.md) | GET | Retrieves a project from Filestage by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Filestage. |
| [Move Project to a Folder](actions/move-project-to-a-folder.md) | PUT | Moves a Filestage project to a folder. |
| [Remove Project by ID](actions/remove-project-by-id.md) | DELETE | Deletes a project from Filestage by ID. |
| [Rename Project by ID](actions/rename-project-by-id.md) | PUT | Updates a Filestage project name by ID. |

### Project Template

| Action | Method | Description |
| --- | --- | --- |
| [Create New Project Template](actions/create-new-project-template.md) | POST | Creates a new project template in Filestage. |
| [List Project Templates](actions/list-project-templates.md) | GET | Retrieves project templates from Filestage. |
| [Remove Project Template](actions/remove-project-template.md) | DELETE | Deletes a project template from Filestage. |
| [Rename Project Template](actions/rename-project-template.md) | PUT | Updates a project template name in Filestage. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Approve a Version](actions/approve-a-version.md) | POST | Approves a Filestage review version. |
| [Approve a Version With Changes](actions/approve-a-version-with-changes.md) | POST | Approves a Filestage review version with changes. |
| [Get Review by ID](actions/get-review-by-id.md) | GET | Retrieves a review from Filestage by ID. |
| [List File Reviews](actions/list-file-reviews.md) | GET | Retrieves reviews for a Filestage file. |
| [List File Reviews by Parameters](actions/list-file-reviews-by-parameters.md) | GET | Finds Filestage file reviews by parameter. |
| [List Reviews for a Reviewer Group](actions/list-reviews-for-a-reviewer-group.md) | GET | Retrieves reviews for a Filestage reviewer group. |
| [Reject a Version](actions/reject-a-version.md) | POST | Rejects a Filestage review version. |
| [Request Changes](actions/request-changes.md) | POST | Requests changes for a Filestage review version. |
| [Set Review Due Date](actions/set-review-due-date.md) | PUT | Sets a due date for a Filestage review. |
| [Start a Review](actions/start-a-review.md) | POST | Starts a review in Filestage. |
| [Undo Review Decision](actions/undo-review-decision.md) | DELETE | Deletes a review decision from Filestage. |
| [Update Review Status](actions/update-review-status.md) | PUT | Updates a review status in Filestage. |

### Review Decision

| Action | Method | Description |
| --- | --- | --- |
| [Submit a Review Decision](actions/submit-a-review-decision.md) | POST | Submits a review decision in Filestage. |

### Review Decision Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Decision Count](actions/get-review-decision-count.md) | GET | Retrieves review decision counts from a Filestage section. |

### Review Report

| Action | Method | Description |
| --- | --- | --- |
| [Download Review Report of File](actions/download-review-report-of-file.md) | GET | Downloads a review report for a Filestage file. |
| [Download Review Report of Review](actions/download-review-report-of-review.md) | GET | Downloads a review report for a Filestage review. |

### Reviewer Group

| Action | Method | Description |
| --- | --- | --- |
| [Add Reviewer Group to Project](actions/add-reviewer-group-to-project.md) | POST | Creates a reviewer group in a Filestage project. |
| [Add Reviewer Group to Project Template](actions/add-reviewer-group-to-project-template.md) | POST | Creates a reviewer group in a Filestage project template. |
| [Add Reviewers to Reviewer Group](actions/add-reviewers-to-reviewer-group.md) | POST | Adds reviewers to a Filestage reviewer group. |
| [Get Reviewer Group by ID](actions/get-reviewer-group-by-id.md) | GET | Retrieves a reviewer group from Filestage by ID. |
| [List Reviewer Groups by Project](actions/list-reviewer-groups-by-project.md) | GET | Retrieves reviewer groups from a Filestage project. |
| [Remove Reviewer Group](actions/remove-reviewer-group.md) | DELETE | Deletes a reviewer group from Filestage. |
| [Remove Reviewers from Reviewer Group](actions/remove-reviewers-from-reviewer-group.md) | DELETE | Deletes reviewers from a Filestage reviewer group. |
| [Rename Reviewer Group](actions/rename-reviewer-group.md) | PUT | Updates a reviewer group name in Filestage. |
| [Update Reviewer Group Settings](actions/update-reviewer-group-settings.md) | PUT | Updates settings for a Filestage reviewer group. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Add New Section](actions/add-new-section.md) | POST | Creates a new section in a Filestage project. |
| [Add Section to Project Template](actions/add-section-to-project-template.md) | POST | Creates a section in a Filestage project template. |
| [Move Section](actions/move-section.md) | PUT | Moves a section to a new position in Filestage. |
| [Remove Section](actions/remove-section.md) | DELETE | Deletes a section from a Filestage project. |
| [Rename Section](actions/rename-section.md) | PUT | Updates a section name in Filestage. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Invite Team Member](actions/invite-team-member.md) | POST | Creates a new team member invitation in Filestage. |
| [Invite Team Members](actions/invite-team-members.md) | POST | Creates team member invitations in Filestage. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Filestage. |
| [Remove Team Member by Email or IdP ID](actions/remove-team-member-by-email-or-idp-id.md) | DELETE | Deletes a Filestage team member by email or IdP ID. |
| [Remove Team Member by Member ID](actions/remove-team-member-by-member-id.md) | DELETE | Deletes a Filestage team member by member ID. |
| [Update Role of Team Member](actions/update-role-of-team-member.md) | PUT | Updates a team member role in Filestage. |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates a team member in Filestage. |

### Team Role

| Action | Method | Description |
| --- | --- | --- |
| [List Team Roles](actions/list-team-roles.md) | GET | Retrieves team roles from Filestage. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add New Webhook](actions/add-new-webhook.md) | POST | Creates a new webhook in Filestage. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Filestage. |
| [Remove Webhook by ID](actions/remove-webhook-by-id.md) | DELETE | Deletes a webhook from Filestage by ID. |
| [Update Webhook by ID](actions/update-webhook-by-id.md) | PUT | Updates a webhook in Filestage by ID. |

