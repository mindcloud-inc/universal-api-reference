# Filestage: Native API Reference

A consolidated summary of Filestage's API configuration and 81 documented operations, with links to official documentation.

- **Official docs:** https://developers.filestage.io/docs/api/a3dwkuuqd37h7-welcome-to-our-api-reference
- **OpenAPI specification:** https://developers.filestage.io/api/v1/projects/filestage/api/nodes/%2FFilestage%20API%20V2.oas3.json?branch=main
- **API base URL:** `https://api.filestage.io/ext/v2`

## Authentication

### API Key

Connect with a Filestage API key. Filestage documents bearer-token authentication through the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.filestage.io/docs/api/ZG9jOjg2MDMzNQ-authentication)

## Endpoints (81 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Collaborators to Project](actions/add-collaborators-to-project.md) | `POST /projects/{projectId}/collaborators` | [docs](https://developers.filestage.io/docs/api/xi8qqsa786l43-add-collaborators-to-project) |
| [Add New Section](actions/add-new-section.md) | `POST /projects/{projectId}/sections` | [docs](https://developers.filestage.io/docs/api/vcqwuhq2ejw8y-add-new-section) |
| [Add New Webhook](actions/add-new-webhook.md) | `POST /webhooks` | [docs](https://developers.filestage.io/docs/api/79twjnt5elqnk-add-new-webhook) |
| [Add Reviewer Group to Project](actions/add-reviewer-group-to-project.md) | `POST /steps` | [docs](https://developers.filestage.io/docs/api/d6pww0n8354za-add-reviewer-group-to-project) |
| [Add Reviewer Group to Project Template](actions/add-reviewer-group-to-project-template.md) | `POST /project-templates/{projectTemplateId}/steps` | [docs](https://developers.filestage.io/docs/api/a4xce2oplgd79-add-reviewer-group-to-project-template) |
| [Add Reviewers to Reviewer Group](actions/add-reviewers-to-reviewer-group.md) | `POST /steps/{stepId}/reviewers` | [docs](https://developers.filestage.io/docs/api/9082lw60y3i2v-add-reviewers-to-reviewer-group) |
| [Add Section to Project Template](actions/add-section-to-project-template.md) | `POST /project-templates/{projectTemplateId}/sections` | [docs](https://developers.filestage.io/docs/api/651rufwgkc4fi-add-section-to-project-template) |
| [Approve a Version](actions/approve-a-version.md) | `POST /reviews/{reviewId}/approve` | [docs](https://developers.filestage.io/docs/api/bl3h108vb7qfj-approve-a-version) |
| [Approve a Version With Changes](actions/approve-a-version-with-changes.md) | `POST /reviews/{reviewId}/approve-with-changes` | [docs](https://developers.filestage.io/docs/api/esma0fr0ql07c-approve-a-version-with-changes) |
| [Archive or Unarchive Project by ID](actions/archive-or-unarchive-project-by-id.md) | `PUT /projects/{projectId}/isArchived` | [docs](https://developers.filestage.io/docs/api/riodpev6z6775-archive-unarchive-project-by-id) |
| [Copy Comments Between Versions or Reviews](actions/copy-comments-between-versions-or-reviews.md) | `POST /reviews/{reviewId}/comments/copy` | [docs](https://developers.filestage.io/docs/api/28m6vxw2bt6tx-copy-comments-between-versions-or-reviews) |
| [Create Comment Reply](actions/create-comment-reply.md) | `POST /comments/{commentId}/replies` | [docs](https://developers.filestage.io/docs/api/u2y9vi6ddo0ul-create-comment-reply) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://developers.filestage.io/docs/api/km0e5pq67m95m-create-folder) |
| [Create New Project Template](actions/create-new-project-template.md) | `POST /project-templates` | [docs](https://developers.filestage.io/docs/api/gbp5tkhkneye5-create-new-project-template) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.filestage.io/docs/api/3ifqfpvkrrtct-create-project) |
| [Create Review Comment](actions/create-review-comment.md) | `POST /reviews/{reviewId}/comments` | [docs](https://developers.filestage.io/docs/api/3rj5isxwlfnwu-create-review-comment) |
| [Download Comment Attachment](actions/download-comment-attachment.md) | `GET /comments/{commentId}/attachments/{attachmentId}/contents` | [docs](https://developers.filestage.io/docs/api/ymynmgcr9km61-download-comment-attachment) |
| [Download File Version](actions/download-file-version.md) | `GET /versions/{versionId}/contents` | [docs](https://developers.filestage.io/docs/api/zjznxwryl60f7-download-file-version) |
| [Download Review Report of File](actions/download-review-report-of-file.md) | `GET /files/{fileId}/report` | [docs](https://developers.filestage.io/docs/api/8f7a68yac21ff-download-review-report-of-file) |
| [Download Review Report of Review](actions/download-review-report-of-review.md) | `GET /reviews/{reviewId}/report` | [docs](https://developers.filestage.io/docs/api/wwjic2o2f4m2r-download-review-report-of-review) |
| [Generate Presigned Upload URL](actions/generate-presigned-upload-url.md) | `POST /files/upload-url` | [docs](https://developers.filestage.io/docs/api/dxto43ie83w98-generate-presigned-upload-url) |
| [Get Comment](actions/get-comment.md) | `GET /comments/{commentId}` | [docs](https://developers.filestage.io/docs/api/svpjaocu9js3z-get-comment) |
| [Get File by ID](actions/get-file-by-id.md) | `GET /files/{fileId}` | [docs](https://developers.filestage.io/docs/api/t6rimdwbnx4rt-get-file-by-id) |
| [Get File URL](actions/get-file-url.md) | `GET /versions/{versionId}/fileDatas/url` | [docs](https://developers.filestage.io/docs/api/yvzft64lktvar-get-file-url) |
| [Get Folder by ID](actions/get-folder-by-id.md) | `GET /folders/{folderId}` | [docs](https://developers.filestage.io/docs/api/edi8abom371wf-get-folder-by-id) |
| [Get Project by ID](actions/get-project-by-id.md) | `GET /projects/{projectId}` | [docs](https://developers.filestage.io/docs/api/sfo3vv07mr128-get-project-by-id) |
| [Get Review by ID](actions/get-review-by-id.md) | `GET /reviews/{reviewId}` | [docs](https://developers.filestage.io/docs/api/idzslehyfp37z-get-review-by-id) |
| [Get Review Decision Count](actions/get-review-decision-count.md) | `GET /sections/{sectionId}/reviews/status/count` | [docs](https://developers.filestage.io/docs/api/tfo8lt6wpzuxk-number-of-review-decisions) |
| [Get Reviewer Group by ID](actions/get-reviewer-group-by-id.md) | `GET /steps/{stepId}` | [docs](https://developers.filestage.io/docs/api/el174yzb9c3um-get-reviewer-group-by-id) |
| [Import Website](actions/import-website.md) | `POST /files/import-website` | [docs](https://developers.filestage.io/docs/api/0gstxpcjbyadr-import-website) |
| [Invite Team Member](actions/invite-team-member.md) | `POST /team/members` | [docs](https://developers.filestage.io/docs/api/5v0lokos961fz-invite-team-member) |
| [Invite Team Members](actions/invite-team-members.md) | `POST /team/members/{memberId}` | [docs](https://developers.filestage.io/docs/api/bs3ac0u9uffxk-invite-team-members) |
| [List Comments by Review](actions/list-comments-by-review.md) | `GET /reviews/{reviewId}/comments` | [docs](https://developers.filestage.io/docs/api/l2twb6d5i18my-get-comments-by-review) |
| [List File Reviews](actions/list-file-reviews.md) | `GET /files/{fileId}/reviews` | [docs](https://developers.filestage.io/docs/api/bb3tlfor3cocg-get-file-reviews) |
| [List File Reviews by Parameters](actions/list-file-reviews-by-parameters.md) | `GET /files/reviews` | [docs](https://developers.filestage.io/docs/api/mrkvlsdu1r54p-get-files-reviews-by-parameters) |
| [List Files by Parameters](actions/list-files-by-parameters.md) | `GET /files` | [docs](https://developers.filestage.io/docs/api/9za81gw5tvkc3-get-files-by-parameters) |
| [List Files by Project](actions/list-files-by-project.md) | `GET /projects/{projectId}/files` | [docs](https://developers.filestage.io/docs/api/uedfk1htj4qvf-get-files-by-project) |
| [List Files in Section](actions/list-files-in-section.md) | `GET /sections/{sectionId}/files` | [docs](https://developers.filestage.io/docs/api/bb86bv2rotkox-get-files-in-section) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://developers.filestage.io/docs/api/kr1wzpnzik41i-get-folders) |
| [List Mention Suggestions](actions/list-mention-suggestions.md) | `GET /steps/{stepId}/mention-suggestions` | [docs](https://developers.filestage.io/docs/api/i6yb0mvykt4ru-get-mention-suggestions) |
| [List Project Templates](actions/list-project-templates.md) | `GET /project-templates` | [docs](https://developers.filestage.io/docs/api/j7p98elyaunwp-get-project-templates) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.filestage.io/docs/api/afbeftkcpp5yd-get-projects) |
| [List Reviewer Groups by Project](actions/list-reviewer-groups-by-project.md) | `GET /projects/{projectId}/steps` | [docs](https://developers.filestage.io/docs/api/pojhx8u6q36m6-get-reviewer-groups-by-project) |
| [List Reviews for a Reviewer Group](actions/list-reviews-for-a-reviewer-group.md) | `GET /steps/{stepId}/reviews` | [docs](https://developers.filestage.io/docs/api/a1b2c3d4e5f6g-get-reviews-for-a-review-group) |
| [List Team Members](actions/list-team-members.md) | `GET /team/members` | [docs](https://developers.filestage.io/docs/api/ry33j5vt8rpcs-get-team-members) |
| [List Team Roles](actions/list-team-roles.md) | `GET /team/roles` | [docs](https://developers.filestage.io/docs/api/flp2tp0jr8urf-get-team-roles) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.filestage.io/docs/api/pfagr4mr3chop-get-webhooks) |
| [Move File to a Section](actions/move-file-to-a-section.md) | `PUT /files/{fileId}/section` | [docs](https://developers.filestage.io/docs/api/mi9lh0smo12di-move-file-to-a-section) |
| [Move Project to a Folder](actions/move-project-to-a-folder.md) | `PUT /projects/{projectId}/folder` | [docs](https://developers.filestage.io/docs/api/yc164fkzqem9p-move-project-to-a-folder) |
| [Move Section](actions/move-section.md) | `PUT /projects/{projectId}/sections/{sectionId}/position` | [docs](https://developers.filestage.io/docs/api/p3sv3uy7khxb5-move-section) |
| [Pin or Unpin a Comment](actions/pin-or-unpin-a-comment.md) | `PUT /comments/{commentId}/pinned` | [docs](https://developers.filestage.io/docs/api/u4tj3rcpol3g0-pin-or-unpin-a-comment) |
| [Reject a Version](actions/reject-a-version.md) | `POST /reviews/{reviewId}/reject` | [docs](https://developers.filestage.io/docs/api/a6lulqg6zfp12-reject-a-version) |
| [Remove Collaborator](actions/remove-collaborator.md) | `DELETE /projects/{projectId}/collaborators/{collaboratorId}` | [docs](https://developers.filestage.io/docs/api/zrnm39e80f9pl-remove-collaborator) |
| [Remove Comment](actions/remove-comment.md) | `DELETE /comments/{commentId}` | [docs](https://developers.filestage.io/docs/api/99do8o0x8cv8d-remove-comment) |
| [Remove File](actions/remove-file.md) | `DELETE /files/{fileId}` | [docs](https://developers.filestage.io/docs/api/1oshr8x026hcw-remove-file) |
| [Remove File by External ID](actions/remove-file-by-external-id.md) | `DELETE /files` | [docs](https://developers.filestage.io/docs/api/oh7eqeplqtm9s-remove-file-by-external-id) |
| [Remove Project by ID](actions/remove-project-by-id.md) | `DELETE /projects/{projectId}` | [docs](https://developers.filestage.io/docs/api/hmd9lnnpmf79o-remove-project-by-id) |
| [Remove Project Template](actions/remove-project-template.md) | `DELETE /project-templates/{projectTemplateId}` | [docs](https://developers.filestage.io/docs/api/n61dfggl3druf-remove-project-template) |
| [Remove Reviewer Group](actions/remove-reviewer-group.md) | `DELETE /steps/{stepId}` | [docs](https://developers.filestage.io/docs/api/8xazw51mw4c0x-remove-reviewer-group) |
| [Remove Reviewers from Reviewer Group](actions/remove-reviewers-from-reviewer-group.md) | `DELETE /steps/{stepId}/reviewer` | [docs](https://developers.filestage.io/docs/api/1kssr3rtqap4w-remove-reviewers-from-reviewer-group) |
| [Remove Section](actions/remove-section.md) | `DELETE /projects/{projectId}/sections/{sectionId}` | [docs](https://developers.filestage.io/docs/api/fotiebmtuj7xt-remove-section) |
| [Remove Team Member by Email or IdP ID](actions/remove-team-member-by-email-or-idp-id.md) | `DELETE /team/members` | [docs](https://developers.filestage.io/docs/api/oadv4f9asb1oe-remove-team-member-by-email-or-idpid) |
| [Remove Team Member by Member ID](actions/remove-team-member-by-member-id.md) | `DELETE /team/members/{memberId}` | [docs](https://developers.filestage.io/docs/api/3h6t5yy5kd534-remove-team-member-by-memberid) |
| [Remove Webhook by ID](actions/remove-webhook-by-id.md) | `DELETE /webhooks/{webhookId}` | [docs](https://developers.filestage.io/docs/api/9chghs3azv2lg-remove-webhook-by-id) |
| [Rename Project by ID](actions/rename-project-by-id.md) | `PUT /projects/{projectId}/name` | [docs](https://developers.filestage.io/docs/api/huaimmzpi8uib-rename-project-by-id) |
| [Rename Project Template](actions/rename-project-template.md) | `PUT /project-templates/{projectTemplateId}` | [docs](https://developers.filestage.io/docs/api/tgmtwbgtrfefq-rename-project-template) |
| [Rename Reviewer Group](actions/rename-reviewer-group.md) | `PUT /steps/{stepId}/name` | [docs](https://developers.filestage.io/docs/api/hi66jjtl28qwg-rename-reviewer-group) |
| [Rename Section](actions/rename-section.md) | `PUT /projects/{projectId}/sections/{sectionId}` | [docs](https://developers.filestage.io/docs/api/3suhqt87go17q-rename-section) |
| [Request Changes](actions/request-changes.md) | `POST /reviews/{reviewId}/request-changes` | [docs](https://developers.filestage.io/docs/api/koplrg8gcmlde-request-changes) |
| [Set Review Due Date](actions/set-review-due-date.md) | `PUT /reviews/{reviewId}/due-date` | [docs](https://developers.filestage.io/docs/api/4e8t7j93p6k0q-set-review-due-date) |
| [Start a Review](actions/start-a-review.md) | `POST /reviews` | [docs](https://developers.filestage.io/docs/api/fv1oow7b8r46b-start-a-review) |
| [Submit a Review Decision](actions/submit-a-review-decision.md) | `POST /review/decision` | [docs](https://developers.filestage.io/docs/api/jsdjk349i23dl-submit-a-review-decision) |
| [Undo Review Decision](actions/undo-review-decision.md) | `DELETE /reviews/{reviewId}/decision` | [docs](https://developers.filestage.io/docs/api/i26y66fo0yywp-undo-review-decision) |
| [Update Comment](actions/update-comment.md) | `PUT /comments/{commentId}` | [docs](https://developers.filestage.io/docs/api/g7s1b9cvzldjh-update-comment) |
| [Update Comment Resolution](actions/update-comment-resolution.md) | `PUT /comments/{commentId}/resolution` | [docs](https://developers.filestage.io/docs/api/pmjv5qalq096u-update-comment-resolution) |
| [Update Review Status](actions/update-review-status.md) | `PUT /reviews/{reviewId}/status` | [docs](https://developers.filestage.io/docs/api/txazpofppz8rd-update-review-status) |
| [Update Reviewer Group Settings](actions/update-reviewer-group-settings.md) | `PUT /steps/{stepId}/settings` | [docs](https://developers.filestage.io/docs/api/hjfk7udk1cx3k-update-reviewer-group-settings) |
| [Update Role of Team Member](actions/update-role-of-team-member.md) | `PUT /team/members/{memberId}/role` | [docs](https://developers.filestage.io/docs/api/ilqk7tdu1swil-update-role-of-team-member) |
| [Update Team Member](actions/update-team-member.md) | `PUT /team/members/{memberId}` | [docs](https://developers.filestage.io/docs/api/93vg9wo9b797d-update-team-member) |
| [Update Webhook by ID](actions/update-webhook-by-id.md) | `PUT /webhooks/{webhookId}` | [docs](https://developers.filestage.io/docs/api/81v5wkyjfcm5t-update-webhook-by-id) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://developers.filestage.io/docs/api/1wmibjt5eccjb-upload-file) |
