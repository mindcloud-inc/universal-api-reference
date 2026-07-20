# NetExplorer: Native API Reference

A consolidated summary of NetExplorer's API configuration and 240 documented operations, with links to official documentation.

- **Official docs:** https://api.netexplorer.fr/v3/
- **API base URL:** `{platformBaseUrl}/api`

## Authentication

### OAuth2

Connect a NetExplorer tenant with OAuth2 client-credentials (server-to-server) using a tenant base URL plus the tenant-specific client ID and client secret entered in the connection form.

### Credentials

- **Platform Base URL:** `platformBaseUrl` · required · The full NetExplorer platform base URL, for example `https://company.netexplorer.pro`. Do not include `/api`.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.platformBaseUrl}}/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.platformBaseUrl}}/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


Refresh expired access tokens with a POST request to {{credentials.platformBaseUrl}}/oauth2/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://api.netexplorer.fr/v3/#authorize)

## Endpoints (240 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Update Account Picture](actions/create-account-picture.md) | `POST /account/picture` | [docs](https://api.netexplorer.fr/v3/#account.post.picture) |
| [Create Alert](actions/create-alert.md) | `POST /alert` | [docs](https://api.netexplorer.fr/v3/#alerts.post.create) |
| [Create Annotation](actions/create-annotation.md) | `POST /annotation` | [docs](https://api.netexplorer.fr/v3/#annotations.post.create) |
| [Create Folder](actions/create-archive-folder.md) | `POST /archive/folder` | [docs](https://api.netexplorer.fr/v3/#archive.post.archive-create-folder) |
| [Create Test](actions/create-config-smtp-test.md) | `POST /config/smtp/test` | [docs](https://api.netexplorer.fr/v3/#config.post.test-smtp) |
| [Create Delegate](actions/create-delegate.md) | `POST /delegate` | [docs](https://api.netexplorer.fr/v3/#delegates.post.create) |
| [Create Email](actions/create-email.md) | `POST /email` | [docs](https://api.netexplorer.fr/v3/#emails.post.create) |
| [Create File](actions/create-file.md) | `POST /file` | [docs](https://api.netexplorer.fr/v3/#files.post.create) |
| [Create Tus Upload](actions/create-file-tus.md) | `POST /file/tus` | [docs](https://api.netexplorer.fr/v3/#files.post.tus) |
| [Upload File](actions/create-file-upload.md) | `POST /file/upload` | [docs](https://api.netexplorer.fr/v3/#files.post.upload) |
| [Create Folder](actions/create-folder.md) | `POST /folder` | [docs](https://api.netexplorer.fr/v3/#folders.post.create) |
| [Create Group](actions/create-group.md) | `POST /group` | [docs](https://api.netexplorer.fr/v3/#groups.post.create) |
| [Create Provider](actions/create-identity-provider.md) | `POST /identity/provider` | [docs](https://api.netexplorer.fr/v3/#identity.post.post) |
| [Create Sync](actions/create-identity-provider-by-id-sync.md) | `POST /identity/provider/:id/sync` | [docs](https://api.netexplorer.fr/v3/#identity.post.post-sync) |
| [Create Test](actions/create-identity-provider-test.md) | `POST /identity/provider/test` | [docs](https://api.netexplorer.fr/v3/#identity.post.post-test) |
| [Create Invite](actions/create-invite.md) | `POST /invite` | [docs](https://api.netexplorer.fr/v3/#invitations.post.create) |
| [Create App](actions/create-oauth2-app.md) | `POST /oauth2/app` | [docs](https://api.netexplorer.fr/v3/#oauth2.post.oauth2-post-app) |
| [Reset App Secret](actions/create-oauth2-app-by-client-id-reset.md) | `POST /oauth2/app/:clientId/reset` | [docs](https://api.netexplorer.fr/v3/#oauth2.post.oauth2-post-app-reset) |
| [Reset Password](actions/create-reset-password.md) | `POST /reset_password` | [docs](https://api.netexplorer.fr/v3/#account.post.resetpwd) |
| [Create Right](actions/create-right.md) | `POST /right` | [docs](https://api.netexplorer.fr/v3/#rights.post.create) |
| [Create Share](actions/create-share.md) | `POST /share` | [docs](https://api.netexplorer.fr/v3/#shares.post.share-post) |
| [Create Email](actions/create-share-email.md) | `POST /share/email` | [docs](https://api.netexplorer.fr/v3/#shares-email.post.share-post) |
| [Validate Sharelink Password](actions/create-share-key-by-share-key-passcheck.md) | `POST /share/key/:shareKey/passcheck` | [docs](https://api.netexplorer.fr/v3/#shares.post.shares-passcheck-key) |
| [Send Share SMS](actions/create-share-key-by-share-key-sms.md) | `POST /share/key/:shareKey/sms` | [docs](https://api.netexplorer.fr/v3/#shares.post.shares-sms-key) |
| [Create Sharelink](actions/create-sharelink.md) | `POST /sharelink` | [docs](https://api.netexplorer.fr/v3/#sharelinks.post.create) |
| [Create File](actions/create-sharelink-by-sharelink-id-file.md) | `POST /sharelink/:sharelinkId/file` | [docs](https://api.netexplorer.fr/v3/#sharelinks.post.add-file) |
| [Create Folder](actions/create-sharelink-by-sharelink-id-folder.md) | `POST /sharelink/:sharelinkId/folder` | [docs](https://api.netexplorer.fr/v3/#sharelinks.post.add-folder) |
| [Validate Sharelink Password](actions/create-sharelink-by-sharelink-id-passcheck.md) | `POST /sharelink/:sharelinkId/passcheck` | [docs](https://api.netexplorer.fr/v3/#sharelinks.post.passcheck) |
| [Create Email](actions/create-sharelink-email.md) | `POST /sharelink/email` | [docs](https://api.netexplorer.fr/v3/#sharelinks-email.post.create) |
| [Validate Sharelink Password](actions/create-sharelink-key-by-sharelink-key-passcheck.md) | `POST /sharelink/key/:sharelinkKey/passcheck` | [docs](https://api.netexplorer.fr/v3/#sharelinks.post.passcheck-key) |
| [Create Signature](actions/create-signatures.md) | `POST /signatures` | [docs](https://api.netexplorer.fr/v3/#signature.post.create signature) |
| [Create Activate](actions/create-signatures-by-signature-id-activate.md) | `POST /signatures/:signatureId/activate` | [docs](https://api.netexplorer.fr/v3/#signature.post.activate signature) |
| [Create Actor](actions/create-signatures-by-signature-id-actors.md) | `POST /signatures/:signatureId/actors` | [docs](https://api.netexplorer.fr/v3/#signature.post.add actor) |
| [Create Remind](actions/create-signatures-by-signature-id-actors-by-actor-id-remind.md) | `POST /signatures/:signatureId/actors/:actorId/remind` | [docs](https://api.netexplorer.fr/v3/#signature.post.remind actor) |
| [Create Remind](actions/create-signatures-by-signature-id-actors-remind.md) | `POST /signatures/:signatureId/actors/remind` | [docs](https://api.netexplorer.fr/v3/#signature.post.remind all actors) |
| [Create Cancel](actions/create-signatures-by-signature-id-cancel.md) | `POST /signatures/:signatureId/cancel` | [docs](https://api.netexplorer.fr/v3/#signature.post.cancel signature) |
| [Create Field](actions/create-signatures-by-signature-id-documents-by-document-id-fields.md) | `POST /signatures/:signatureId/documents/:documentId/fields` | [docs](https://api.netexplorer.fr/v3/#signature.post.create field) |
| [Create Document](actions/create-signatures-by-signature-id-documents-by-file-id.md) | `POST /signatures/:signatureId/documents/:fileId` | [docs](https://api.netexplorer.fr/v3/#signature.post.add document) |
| [Create Tag](actions/create-tag.md) | `POST /tag` | [docs](https://api.netexplorer.fr/v3/#tags.post.createTag) |
| [Create Folder](actions/create-tag-by-folder-id-folder.md) | `POST /tag/:folderId/folder` | [docs](https://api.netexplorer.fr/v3/#tags.post.grandRevokeTagOnElement) |
| [Create Tag](actions/create-tag-by-tag-id-by-element-id-by-type.md) | `POST /tag/:tagId/:elementId/:type` | [docs](https://api.netexplorer.fr/v3/#tags.post.addTagOnElement) |
| [Create Category](actions/create-tag-category.md) | `POST /tag/category` | [docs](https://api.netexplorer.fr/v3/#tags.post.createCategory) |
| [Create File](actions/create-template-file.md) | `POST /template/file` | [docs](https://api.netexplorer.fr/v3/#template-files.post.create) |
| [Copy Template File](actions/create-template-file-copy.md) | `POST /template/file/copy` | [docs](https://api.netexplorer.fr/v3/#template-files.post.duplicate) |
| [Generate Token Token](actions/create-token-file-by-file-id-by-type.md) | `POST /token/file/:fileId/:type` | [docs](https://api.netexplorer.fr/v3/#token.post.file) |
| [Generate Token Token](actions/create-token-share-by-guid-by-type-by-key.md) | `POST /token/share/:guId/:type/:key` | [docs](https://api.netexplorer.fr/v3/#token.post.share-file) |
| [Generate Share Download Token](actions/create-token-share-download-by-key.md) | `POST /token/share/download/:key` | [docs](https://api.netexplorer.fr/v3/#token.post.share) |
| [Generate Token Token](actions/create-token-sharelink-by-key-by-data-id-by-type.md) | `POST /token/sharelink/:key/:dataId/:type` | [docs](https://api.netexplorer.fr/v3/#token.post.sharelink_file) |
| [Generate Sharelink Download Token](actions/create-token-sharelink-by-key-download.md) | `POST /token/sharelink/:key/download` | [docs](https://api.netexplorer.fr/v3/#token.post.sharelink) |
| [Generate Token Token](actions/create-token-template-by-id-by-type.md) | `POST /token/template/:id/:type` | [docs](https://api.netexplorer.fr/v3/#token.post.template-file) |
| [Create Ulink](actions/create-ulink.md) | `POST /ulink` | [docs](https://api.netexplorer.fr/v3/#ulinks.post.create) |
| [Create Email](actions/create-ulink-email.md) | `POST /ulink/email` | [docs](https://api.netexplorer.fr/v3/#ulinks-email.post.ulink-email-post) |
| [Validate Sharelink Password](actions/create-ulink-key-by-ulink-key-passcheck.md) | `POST /ulink/key/:ulinkKey/passcheck` | [docs](https://api.netexplorer.fr/v3/#ulinks.post.ulink-passcheck-key) |
| [Send Upload Link SMS](actions/create-ulink-key-by-ulink-key-sms.md) | `POST /ulink/key/:ulinkKey/sms` | [docs](https://api.netexplorer.fr/v3/#ulinks.post.ulink-sms-key) |
| [Create User](actions/create-user.md) | `POST /user` | [docs](https://api.netexplorer.fr/v3/#users.post.create) |
| [Update User Picture](actions/create-user-by-user-id-picture.md) | `POST /user/:userId/picture` | [docs](https://api.netexplorer.fr/v3/#users.post.picture) |
| [Create Instance](actions/create-workflow-instance.md) | `POST /workflow/instance` | [docs](https://api.netexplorer.fr/v3/#workflow.post.create) |
| [Create Share](actions/create-zip-token-share.md) | `POST /zip/token/share` | [docs](https://api.netexplorer.fr/v3/#shares.post.zip-share) |
| [Delete Account Picture](actions/delete-account-picture.md) | `DELETE /account/picture` | [docs](https://api.netexplorer.fr/v3/#account.delete.delete-picture) |
| [Delete Alert](actions/delete-alert-by-alert-id.md) | `DELETE /alert/:alertId` | [docs](https://api.netexplorer.fr/v3/#alerts.delete.delete) |
| [Delete Annotation](actions/delete-annotation-by-annotation-id.md) | `DELETE /annotation/:annotationId` | [docs](https://api.netexplorer.fr/v3/#annotations.delete.delete) |
| [Delete File](actions/delete-archive-file-by-file-id.md) | `DELETE /archive/file/:fileId` | [docs](https://api.netexplorer.fr/v3/#archive.delete.delete-file) |
| [Delete Folder](actions/delete-archive-folder-by-folder-id.md) | `DELETE /archive/folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#archive.delete.delete-folder) |
| [Delete Delegate](actions/delete-delegate-by-delegate-id.md) | `DELETE /delegate/:delegateId` | [docs](https://api.netexplorer.fr/v3/#delegates.delete.delete) |
| [Delete Email](actions/delete-email-by-email-id.md) | `DELETE /email/:emailId` | [docs](https://api.netexplorer.fr/v3/#emails.delete.delete) |
| [Delete File](actions/delete-file-by-file-id.md) | `DELETE /file/:fileId` | [docs](https://api.netexplorer.fr/v3/#files.delete.delete) |
| [Cancel File Upload](actions/delete-file-cancel.md) | `DELETE /file/cancel` | [docs](https://api.netexplorer.fr/v3/#files.delete.cancel-upload) |
| [Delete Folder](actions/delete-folder-by-folder-id.md) | `DELETE /folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#folders.delete.delete) |
| [Delete Group](actions/delete-group-by-group-id.md) | `DELETE /group/:groupId` | [docs](https://api.netexplorer.fr/v3/#groups.delete.delete) |
| [Delete Provider](actions/delete-identity-provider-by-id.md) | `DELETE /identity/provider/:id` | [docs](https://api.netexplorer.fr/v3/#identity.delete.delete) |
| [Delete Invite](actions/delete-invite-by-invite-id.md) | `DELETE /invite/:inviteId` | [docs](https://api.netexplorer.fr/v3/#invitations.delete.delete) |
| [Delete Lock](actions/delete-lock-by-file-id.md) | `DELETE /lock/:fileId` | [docs](https://api.netexplorer.fr/v3/#locks.delete.delete) |
| [Delete App](actions/delete-oauth2-app-by-client-id.md) | `DELETE /oauth2/app/:clientId` | [docs](https://api.netexplorer.fr/v3/#oauth2.delete.oauth2-delete-app) |
| [Revoke App](actions/delete-oauth2-app-by-token-revoke.md) | `DELETE /oauth2/app/:token/revoke` | [docs](https://api.netexplorer.fr/v3/#oauth2.delete.oauth2-revoke-app-token) |
| [Revoke User](actions/delete-oauth2-user-by-token-revoke.md) | `DELETE /oauth2/user/:token/revoke` | [docs](https://api.netexplorer.fr/v3/#oauth2.delete.oauth2-revoke-user-token) |
| [Delete Option](actions/delete-option-by-user-id.md) | `DELETE /option/:userId` | [docs](https://api.netexplorer.fr/v3/#options.delete.delete) |
| [Delete Right](actions/delete-right-by-right-id.md) | `DELETE /right/:rightId` | [docs](https://api.netexplorer.fr/v3/#rights.delete.delete) |
| [Delete Share](actions/delete-share-by-share-id.md) | `DELETE /share/:shareId` | [docs](https://api.netexplorer.fr/v3/#shares.delete.delete) |
| [Delete Email](actions/delete-share-email-by-share-email-id.md) | `DELETE /share/email/:shareEmailId` | [docs](https://api.netexplorer.fr/v3/#shares-email.delete.delete) |
| [Delete Sharelink](actions/delete-sharelink-by-sharelink-id.md) | `DELETE /sharelink/:sharelinkId` | [docs](https://api.netexplorer.fr/v3/#sharelinks.delete.delete) |
| [Delete File](actions/delete-sharelink-by-sharelink-id-file-by-file-id.md) | `DELETE /sharelink/:sharelinkId/file/:fileId` | [docs](https://api.netexplorer.fr/v3/#sharelinks.delete.delete-file) |
| [Delete Email](actions/delete-sharelink-email-by-sharelink-email-id.md) | `DELETE /sharelink/email/:sharelinkEmailId` | [docs](https://api.netexplorer.fr/v3/#sharelinks-email.delete.delete) |
| [Delete Signature](actions/delete-signatures-by-signature-id.md) | `DELETE /signatures/:signatureId` | [docs](https://api.netexplorer.fr/v3/#signature.delete.delete signature) |
| [Delete Actor](actions/delete-signatures-by-signature-id-actors-by-actor-id.md) | `DELETE /signatures/:signatureId/actors/:actorId` | [docs](https://api.netexplorer.fr/v3/#signature.delete.delete actor) |
| [Delete Document](actions/delete-signatures-by-signature-id-documents-by-document-id.md) | `DELETE /signatures/:signatureId/documents/:documentId` | [docs](https://api.netexplorer.fr/v3/#signature.delete.delete document) |
| [Delete Signature Field](actions/delete-signatures-by-signature-id-documents-by-document-id-fields-field-id.md) | `DELETE /signatures/:signatureId/documents/:documentId/fields/:fieldId` | [docs](https://api.netexplorer.fr/v3/#signature.delete.delete field) |
| [Delete Tag](actions/delete-tag-by-tag-id.md) | `DELETE /tag/:tagId` | [docs](https://api.netexplorer.fr/v3/#tags.delete.deleteTag) |
| [Delete Tag](actions/delete-tag-by-tag-id-by-element-id-by-type.md) | `DELETE /tag/:tagId/:elementId/:type` | [docs](https://api.netexplorer.fr/v3/#tags.delete.revokeTagOnElement) |
| [Delete Category](actions/delete-tag-category-by-category-id.md) | `DELETE /tag/category/:categoryId` | [docs](https://api.netexplorer.fr/v3/#tags.delete.deleteCategory) |
| [Delete File](actions/delete-template-file-by-template-id.md) | `DELETE /template/file/:templateId` | [docs](https://api.netexplorer.fr/v3/#template-files.delete.delete) |
| [Delete Trash](actions/delete-trash-by-trash-id.md) | `DELETE /trash/:trashId` | [docs](https://api.netexplorer.fr/v3/#trash.delete.destroy) |
| [Delete Trashe](actions/delete-trashes.md) | `DELETE /trashes` | [docs](https://api.netexplorer.fr/v3/#trash.delete.purge) |
| [Delete Ulink](actions/delete-ulink-by-ulink-id.md) | `DELETE /ulink/:ulinkId` | [docs](https://api.netexplorer.fr/v3/#ulinks.delete.delete) |
| [Delete Email](actions/delete-ulink-email-by-ulink-email-id.md) | `DELETE /ulink/email/:ulinkEmailId` | [docs](https://api.netexplorer.fr/v3/#ulinks-email.delete.delete) |
| [Delete User](actions/delete-user-by-user-id.md) | `DELETE /user/:userId` | [docs](https://api.netexplorer.fr/v3/#users.delete.delete) |
| [Delete User Picture](actions/delete-user-by-user-id-picture.md) | `DELETE /user/:userId/picture` | [docs](https://api.netexplorer.fr/v3/#users.delete.delete-picture) |
| [Delete Instance](actions/delete-workflow-instance-by-instance-id.md) | `DELETE /workflow/instance/:instanceId` | [docs](https://api.netexplorer.fr/v3/#workflow.delete.delete) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://api.netexplorer.fr/v3/#account.get.info) |
| [Get Account Picture](actions/get-account-picture.md) | `GET /account/picture` | [docs](https://api.netexplorer.fr/v3/#account.get.picture) |
| [List File Activity](actions/get-activity-file-by-file-id.md) | `GET /activity/file/:fileId` | [docs](https://api.netexplorer.fr/v3/#activity.get.activity_file) |
| [List Folder Activity](actions/get-activity-folder-by-folder-id.md) | `GET /activity/folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#activity.get.activity_folder) |
| [Get Alert By Alert ID](actions/get-alert-by-alert-id.md) | `GET /alert/:alertId` | [docs](https://api.netexplorer.fr/v3/#alerts.get.fetch) |
| [List Alerts](actions/get-alerts-by-folder-id.md) | `GET /alerts/:folderId` | [docs](https://api.netexplorer.fr/v3/#alerts.get.fetch-all) |
| [Get Annotation By Annotation ID](actions/get-annotation-by-annotation-id.md) | `GET /annotation/:annotationId` | [docs](https://api.netexplorer.fr/v3/#annotations.get.fetch) |
| [Get All](actions/get-annotations-all.md) | `GET /annotations/all` | [docs](https://api.netexplorer.fr/v3/#annotations.get.fetch-all) |
| [List Annotations](actions/get-annotations-by-target-id-by-type.md) | `GET /annotations/:targetId/:type` | [docs](https://api.netexplorer.fr/v3/#annotations.get.fetch-all-target) |
| [Get File](actions/get-archive-file-by-file-id.md) | `GET /archive/file/:fileId` | [docs](https://api.netexplorer.fr/v3/#archive.get.fetch-file) |
| [Get Folder](actions/get-archive-folder-by-folder-id.md) | `GET /archive/folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#archive.get.fetch-folder) |
| [Get Config](actions/get-config.md) | `GET /config` | [docs](https://api.netexplorer.fr/v3/#config.get.fetch) |
| [Get Delegate By Delegate ID](actions/get-delegate-by-delegate-id.md) | `GET /delegate/:delegateId` | [docs](https://api.netexplorer.fr/v3/#delegates.get.fetch) |
| [List Delegates](actions/get-delegates-by-group-id.md) | `GET /delegates/:groupId` | [docs](https://api.netexplorer.fr/v3/#delegates.get.fetch-all) |
| [Get Email By Email ID](actions/get-email-by-email-id.md) | `GET /email/:emailId` | [docs](https://api.netexplorer.fr/v3/#emails.get.fetch) |
| [List Emails](actions/get-emails.md) | `GET /emails` | [docs](https://api.netexplorer.fr/v3/#emails.get.fetch-all) |
| [Get Activity](actions/get-file-activity.md) | `GET /file/activity` | [docs](https://api.netexplorer.fr/v3/#files.get.activity) |
| [Get File By File ID](actions/get-file-by-file-id.md) | `GET /file/:fileId` | [docs](https://api.netexplorer.fr/v3/#files.get.fetch) |
| [Download File By File ID](actions/get-file-by-file-id-download.md) | `GET /file/:fileId/download` | [docs](https://api.netexplorer.fr/v3/#files.get.download) |
| [Get File Info](actions/get-file-by-file-id-infos.md) | `GET /file/:fileId/infos` | [docs](https://api.netexplorer.fr/v3/#files.get.infos) |
| [Get File Timeline](actions/get-file-by-file-id-timeline.md) | `GET /file/:fileId/timeline` | [docs](https://api.netexplorer.fr/v3/#files.get.timeline) |
| [List File Versions](actions/get-file-by-file-id-versions.md) | `GET /file/:fileId/versions` | [docs](https://api.netexplorer.fr/v3/#files.get.versions) |
| [Download File](actions/get-file-download.md) | `GET /file/download` | [docs](https://api.netexplorer.fr/v3/#files.get.token-download) |
| [Get Folder By Folder ID](actions/get-folder-by-folder-id.md) | `GET /folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#folders.get.fetch) |
| [Get Folder Timeline](actions/get-folder-by-folder-id-timeline.md) | `GET /folder/:folderId/timeline` | [docs](https://api.netexplorer.fr/v3/#folders.get.timeline) |
| [List Folders](actions/get-folders.md) | `GET /folders` | [docs](https://api.netexplorer.fr/v3/#folders.get.roots) |
| [Get Fzen](actions/get-fzen.md) | `GET /fzen` | [docs](https://api.netexplorer.fr/v3/#admin.get.fetch) |
| [Get Group By Group ID](actions/get-group-by-group-id.md) | `GET /group/:groupId` | [docs](https://api.netexplorer.fr/v3/#groups.get.fetch) |
| [List Groups](actions/get-groups.md) | `GET /groups` | [docs](https://api.netexplorer.fr/v3/#groups.get.fetch-all) |
| [Get Provider](actions/get-identity-provider-by-id.md) | `GET /identity/provider/:id` | [docs](https://api.netexplorer.fr/v3/#identity.get.get) |
| [Get Matching](actions/get-identity-provider-by-id-matching.md) | `GET /identity/provider/:id/matching` | [docs](https://api.netexplorer.fr/v3/#identity.get.get-matching) |
| [Get Provider](actions/get-identity-providers.md) | `GET /identity/providers` | [docs](https://api.netexplorer.fr/v3/#identity.get.list) |
| [Get User](actions/get-invite-users-by-folder-id.md) | `GET /invite/users/:folderId` | [docs](https://api.netexplorer.fr/v3/#invitations.get.invite-user) |
| [List Invites](actions/get-invites-by-folder-id.md) | `GET /invites/:folderId` | [docs](https://api.netexplorer.fr/v3/#invitations.get.fetch) |
| [Get Ischildof](actions/get-ischildof.md) | `GET /ischildof` | [docs](https://api.netexplorer.fr/v3/#sync.get.ischildof) |
| [Get Lock By File ID](actions/get-lock-by-file-id.md) | `GET /lock/:fileId` | [docs](https://api.netexplorer.fr/v3/#locks.get.fetch) |
| [List Locks](actions/get-locks-by-folder-id.md) | `GET /locks/:folderId` | [docs](https://api.netexplorer.fr/v3/#locks.get.fetch-all) |
| [Get Log By Log ID](actions/get-log-by-log-id.md) | `GET /log/:logId` | [docs](https://api.netexplorer.fr/v3/#logs.get.fetch) |
| [List Logs](actions/get-logs.md) | `GET /logs` | [docs](https://api.netexplorer.fr/v3/#logs.get.fetch-all) |
| [Get Mixer By File ID](actions/get-mixer-by-file-id.md) | `GET /mixer/:fileId` | [docs](https://api.netexplorer.fr/v3/#preview.get.thumbnail) |
| [Get App](actions/get-oauth2-app-by-client-id.md) | `GET /oauth2/app/:clientId` | [docs](https://api.netexplorer.fr/v3/#oauth2.get.oauth2-single) |
| [Get Icon](actions/get-oauth2-app-by-client-id-icon.md) | `GET /oauth2/app/:clientId/icon` | [docs](https://api.netexplorer.fr/v3/#oauth2.get.oauth2-single-icon) |
| [Get Token](actions/get-oauth2-app-by-client-id-tokens.md) | `GET /oauth2/app/:clientId/tokens` | [docs](https://api.netexplorer.fr/v3/#oauth2.get.oauth2-app-tokens) |
| [Get App](actions/get-oauth2-apps.md) | `GET /oauth2/apps` | [docs](https://api.netexplorer.fr/v3/#oauth2.get.oauth2-apps) |
| [Get Token](actions/get-oauth2-user-tokens.md) | `GET /oauth2/user/tokens` | [docs](https://api.netexplorer.fr/v3/#oauth2.get.oauth2-user-tokens) |
| [Get Objectpath](actions/get-objectpath.md) | `GET /objectpath` | [docs](https://api.netexplorer.fr/v3/#sync.get.objectpath) |
| [Get Option By User ID](actions/get-option-by-user-id.md) | `GET /option/:userId` | [docs](https://api.netexplorer.fr/v3/#options.get.fetch) |
| [Get Path](actions/get-path.md) | `GET /path` | [docs](https://api.netexplorer.fr/v3/#sync.get.path) |
| [Get Preview By File ID](actions/get-preview-by-file-id.md) | `GET /preview/:fileId` | [docs](https://api.netexplorer.fr/v3/#preview.get.open) |
| [Get Publicconfig](actions/get-publicconfig.md) | `GET /publicconfig` | [docs](https://api.netexplorer.fr/v3/#config.get.fetch-public) |
| [List Quotas](actions/get-quotas.md) | `GET /quotas` | [docs](https://api.netexplorer.fr/v3/#sync.get.quotas) |
| [Get Right By Right ID](actions/get-right-by-right-id.md) | `GET /right/:rightId` | [docs](https://api.netexplorer.fr/v3/#rights.get.fetch) |
| [List Rights](actions/get-rights-by-folder-id.md) | `GET /rights/:folderId` | [docs](https://api.netexplorer.fr/v3/#rights.get.fetch-all) |
| [Get Root By Type](actions/get-root-by-type.md) | `GET /root/:type` | [docs](https://api.netexplorer.fr/v3/#roots.get.index) |
| [Get Portal Root](actions/get-root-portal-by-filter.md) | `GET /root/portal/:filter` | [docs](https://api.netexplorer.fr/v3/#roots.get.index) |
| [List Roots](actions/get-roots.md) | `GET /roots` | [docs](https://api.netexplorer.fr/v3/#roots.get.index) |
| [Get Share By Share ID](actions/get-share-by-share-id.md) | `GET /share/:shareId` | [docs](https://api.netexplorer.fr/v3/#shares.get.fetch-share) |
| [Get Activity](actions/get-share-by-share-id-activity.md) | `GET /share/:shareId/activity` | [docs](https://api.netexplorer.fr/v3/#shares.get.share-activity) |
| [Get Share Content](actions/get-share-content-by-share-key-folder-id.md) | `GET /share/content/:shareKey/[:folderId]` | [docs](https://api.netexplorer.fr/v3/#shares.get.fetch-content-share) |
| [Get File](actions/get-share-download-file.md) | `GET /share/download/file` | [docs](https://api.netexplorer.fr/v3/#shares.get.share-download-file) |
| [Get Email](actions/get-share-email-by-share-email-id.md) | `GET /share/email/:shareEmailId` | [docs](https://api.netexplorer.fr/v3/#shares-email.get.fetch) |
| [Get Activity](actions/get-share-email-by-share-email-id-activity.md) | `GET /share/email/:shareEmailId/activity` | [docs](https://api.netexplorer.fr/v3/#shares-email.get.share-email-activity) |
| [Get Key](actions/get-share-key-by-share-key.md) | `GET /share/key/:shareKey` | [docs](https://api.netexplorer.fr/v3/#shares.get.fetch-key) |
| [Get Sharelink By Sharelink ID](actions/get-sharelink-by-sharelink-id.md) | `GET /sharelink/:sharelinkId` | [docs](https://api.netexplorer.fr/v3/#sharelinks.get.fetch) |
| [Download Sharelink By Sharelink Key](actions/get-sharelink-download-by-sharelink-key.md) | `GET /sharelink/download/:sharelinkKey` | [docs](https://api.netexplorer.fr/v3/#sharelinks.get.fetch-download) |
| [Get Email](actions/get-sharelink-email-by-sharelink-email-id.md) | `GET /sharelink/email/:sharelinkEmailId` | [docs](https://api.netexplorer.fr/v3/#sharelinks-email.get.fetch) |
| [Get Key](actions/get-sharelink-key-by-sharelink-key.md) | `GET /sharelink/key/:sharelinkKey` | [docs](https://api.netexplorer.fr/v3/#sharelinks.get.fetch-key) |
| [List Sharelinks](actions/get-sharelinks.md) | `GET /sharelinks` | [docs](https://api.netexplorer.fr/v3/#sharelinks.get.fetch-all) |
| [Get Email](actions/get-sharelinks-emails.md) | `GET /sharelinks/emails` | [docs](https://api.netexplorer.fr/v3/#sharelinks-email.get.fetch-all) |
| [List Shares](actions/get-shares.md) | `GET /shares` | [docs](https://api.netexplorer.fr/v3/#shares.get.fetch-shares) |
| [Get Email](actions/get-shares-emails.md) | `GET /shares/emails` | [docs](https://api.netexplorer.fr/v3/#shares-email.get.fetch-all) |
| [List Signatures](actions/get-signatures.md) | `GET /signatures` | [docs](https://api.netexplorer.fr/v3/#signature.get.fetchAll) |
| [List Signatures](actions/get-signatures-by-signature-id.md) | `GET /signatures/:signatureId` | [docs](https://api.netexplorer.fr/v3/#signature.get.fetch) |
| [Get Activity](actions/get-signatures-by-signature-id-activities.md) | `GET /signatures/:signatureId/activities` | [docs](https://api.netexplorer.fr/v3/#signature.get.fetch activities) |
| [Get Export](actions/get-signatures-by-signature-id-activities-export.md) | `GET /signatures/:signatureId/activities/export` | [docs](https://api.netexplorer.fr/v3/#signature.get.export signature activities) |
| [Get Audit](actions/get-signatures-by-signature-id-actors-audit.md) | `GET /signatures/:signatureId/actors/audit` | [docs](https://api.netexplorer.fr/v3/#signature.get.download all audit trail) |
| [Get Audit](actions/get-signatures-by-signature-id-actors-by-actor-id-audit.md) | `GET /signatures/:signatureId/actors/:actorId/audit` | [docs](https://api.netexplorer.fr/v3/#signature.get.download audit trail) |
| [Get Signed](actions/get-signatures-by-signature-id-documents-by-document-id-signed.md) | `GET /signatures/:signatureId/documents/:documentId/signed` | [docs](https://api.netexplorer.fr/v3/#signature.get.download signed document) |
| [Get Signed](actions/get-signatures-by-signature-id-documents-signed.md) | `GET /signatures/:signatureId/documents/signed` | [docs](https://api.netexplorer.fr/v3/#signature.get.download all signed document) |
| [Get Export](actions/get-signatures-export.md) | `GET /signatures/export` | [docs](https://api.netexplorer.fr/v3/#signature.get.export signature requested) |
| [Get Received](actions/get-signatures-received.md) | `GET /signatures/received` | [docs](https://api.netexplorer.fr/v3/#signature.get.fetch received) |
| [Get Export](actions/get-signatures-received-export.md) | `GET /signatures/received/export` | [docs](https://api.netexplorer.fr/v3/#signature.get.export signature received) |
| [Get Tag By Tag ID](actions/get-tag-by-tag-id.md) | `GET /tag/:tagId` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchTag) |
| [Get Category](actions/get-tag-categories.md) | `GET /tag/categories` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchAllCategories) |
| [Get Attached](actions/get-tag-categories-attached-by-element-id-by-type.md) | `GET /tag/categories/attached/:elementId/:type` | [docs](https://api.netexplorer.fr/v3/#tags.get.getAllCategoryOnElement) |
| [Get Category](actions/get-tag-categories-by-element-id-by-type.md) | `GET /tag/categories/:elementId/:type` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchAllCategoriesFromElement) |
| [Get Category](actions/get-tag-category-by-category-id.md) | `GET /tag/category/:categoryId` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchCategory) |
| [Get Category](actions/get-tag-category-by-category-id-by-element-id-by-type.md) | `GET /tag/category/:categoryId/:elementId/:type` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchTagCategoryFromElement) |
| [List Tags](actions/get-tags.md) | `GET /tags` | [docs](https://api.netexplorer.fr/v3/#tags.get.fetchAllTag) |
| [Get Color](actions/get-tags-colors.md) | `GET /tags/colors` | [docs](https://api.netexplorer.fr/v3/#tags.get.getColors) |
| [List Template Files](actions/get-template-files-by-folder-id.md) | `GET /template/files/:folderId` | [docs](https://api.netexplorer.fr/v3/#template-files.get.files) |
| [Get Template Folder](actions/get-template-folder.md) | `GET /template/folder` | [docs](https://api.netexplorer.fr/v3/#template-files.get.fetch) |
| [Get Trash By Trash ID](actions/get-trash-by-trash-id.md) | `GET /trash/:trashId` | [docs](https://api.netexplorer.fr/v3/#trash.get.fetch) |
| [List Trashes](actions/get-trashes.md) | `GET /trashes` | [docs](https://api.netexplorer.fr/v3/#trash.get.fetch-all) |
| [Get Ulink By Ulink ID](actions/get-ulink-by-ulink-id.md) | `GET /ulink/:ulinkId` | [docs](https://api.netexplorer.fr/v3/#ulinks.get.fetch) |
| [Get Email](actions/get-ulink-email-by-ulink-email-id.md) | `GET /ulink/email/:ulinkEmailId` | [docs](https://api.netexplorer.fr/v3/#ulinks-email.get.fetch) |
| [Get Key](actions/get-ulink-key-by-ulink-key.md) | `GET /ulink/key/:ulinkKey` | [docs](https://api.netexplorer.fr/v3/#ulinks.get.fetch-key) |
| [List Ulinks](actions/get-ulinks.md) | `GET /ulinks` | [docs](https://api.netexplorer.fr/v3/#ulinks.get.fetch-all) |
| [Get Email](actions/get-ulinks-emails.md) | `GET /ulinks/emails` | [docs](https://api.netexplorer.fr/v3/#ulinks-email.get.fetch-all) |
| [Get User By User ID](actions/get-user-by-user-id.md) | `GET /user/:userId` | [docs](https://api.netexplorer.fr/v3/#users.get.fetch) |
| [Get User Picture](actions/get-user-by-user-id-picture.md) | `GET /user/:userId/picture` | [docs](https://api.netexplorer.fr/v3/#users.get.picture) |
| [Get User Quota](actions/get-user-by-user-id-quota.md) | `GET /user/:userId/quota` | [docs](https://api.netexplorer.fr/v3/#users.get.quota) |
| [List Users](actions/get-users.md) | `GET /users` | [docs](https://api.netexplorer.fr/v3/#users.get.fetch-all) |
| [Get Instance](actions/get-workflow-instance-by-token.md) | `GET /workflow/instance/:token` | [docs](https://api.netexplorer.fr/v3/#workflow.get.fetch-instance) |
| [Get Instance](actions/get-workflow-instances.md) | `GET /workflow/instances` | [docs](https://api.netexplorer.fr/v3/#workflow.get.fetch-all) |
| [Get Zip](actions/get-zip.md) | `GET /zip` | [docs](https://api.netexplorer.fr/v3/#zip.get.fetch) |
| [Get Share](actions/get-zip-share-by-share-key.md) | `GET /zip/share/:shareKey` | [docs](https://api.netexplorer.fr/v3/#shares.get.download-share) |
| [Update Account](actions/update-account.md) | `PUT /account` | [docs](https://api.netexplorer.fr/v3/#account.put.update) |
| [Update Alert](actions/update-alert-by-alert-id.md) | `PUT /alert/:alertId` | [docs](https://api.netexplorer.fr/v3/#alerts.put.edit) |
| [Update Annotation](actions/update-annotation-by-annotation-id.md) | `PUT /annotation/:annotationId` | [docs](https://api.netexplorer.fr/v3/#annotations.put.edit) |
| [Update All](actions/update-annotations-all.md) | `PUT /annotations/all` | [docs](https://api.netexplorer.fr/v3/#annotations.put.edit-all) |
| [Update File](actions/update-archive-file-by-file-id.md) | `PUT /archive/file/:fileId` | [docs](https://api.netexplorer.fr/v3/#archive.put.file-edit) |
| [Unarchive File](actions/update-archive-file-by-file-id-unarchive.md) | `PUT /archive/file/:fileId/unarchive` | [docs](https://api.netexplorer.fr/v3/#archive.put.file-unarchive) |
| [Update Folder](actions/update-archive-folder-by-folder-id.md) | `PUT /archive/folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#archive.put.folder-edit) |
| [Unarchive Folder](actions/update-archive-folder-by-folder-id-unarchive.md) | `PUT /archive/folder/:folderId/unarchive` | [docs](https://api.netexplorer.fr/v3/#archive.put.folder-unarchive) |
| [Update Config](actions/update-config.md) | `PUT /config` | [docs](https://api.netexplorer.fr/v3/#config.put.update) |
| [Update Delegate](actions/update-delegate-by-delegate-id.md) | `PUT /delegate/:delegateId` | [docs](https://api.netexplorer.fr/v3/#delegates.put.update) |
| [Update Email](actions/update-email-by-email-id.md) | `PUT /email/:emailId` | [docs](https://api.netexplorer.fr/v3/#emails.put.update) |
| [Update File](actions/update-file-by-file-id.md) | `PUT /file/:fileId` | [docs](https://api.netexplorer.fr/v3/#files.put.update) |
| [Archive File](actions/update-file-by-file-id-archive.md) | `PUT /file/:fileId/archive` | [docs](https://api.netexplorer.fr/v3/#archive.put.archive-file-create) |
| [Update File Upload](actions/update-file-by-fileid-upload.md) | `PUT /file/:fileId/upload` | [docs](https://api.netexplorer.fr/v3/#files.put.upload) |
| [Update Folder](actions/update-folder-by-folder-id.md) | `PUT /folder/:folderId` | [docs](https://api.netexplorer.fr/v3/#folders.put.update) |
| [Archive Folder](actions/update-folder-by-folder-id-archive.md) | `PUT /folder/:folderId/archive` | [docs](https://api.netexplorer.fr/v3/#archive.put.archive-folder-create) |
| [Update Group](actions/update-group-by-group-id.md) | `PUT /group/:groupId` | [docs](https://api.netexplorer.fr/v3/#groups.put.update) |
| [Update Provider](actions/update-identity-provider-by-id.md) | `PUT /identity/provider/:id` | [docs](https://api.netexplorer.fr/v3/#identity.put.put) |
| [Update Invite](actions/update-invite-by-invitation-id.md) | `PUT /invite/:invitationId` | [docs](https://api.netexplorer.fr/v3/#invitations.put.edit) |
| [Update Lock](actions/update-lock-by-file-id.md) | `PUT /lock/:fileId` | [docs](https://api.netexplorer.fr/v3/#locks.put.set) |
| [Update App](actions/update-oauth2-app-by-client-id.md) | `PUT /oauth2/app/:clientId` | [docs](https://api.netexplorer.fr/v3/#oauth2.put.oauth2-put-app) |
| [Update Option](actions/update-option-by-user-id.md) | `PUT /option/:userId` | [docs](https://api.netexplorer.fr/v3/#options.put.update) |
| [Update Right](actions/update-right-by-right-id.md) | `PUT /right/:rightId` | [docs](https://api.netexplorer.fr/v3/#rights.put.edit) |
| [Update Share](actions/update-share-by-share-id.md) | `PUT /share/:shareId` | [docs](https://api.netexplorer.fr/v3/#shares.put.share) |
| [Update Email](actions/update-share-email-by-share-email-id.md) | `PUT /share/email/:shareEmailId` | [docs](https://api.netexplorer.fr/v3/#shares-email.put.share) |
| [Update Sharelink](actions/update-sharelink-by-sharelink-id.md) | `PUT /sharelink/:sharelinkId` | [docs](https://api.netexplorer.fr/v3/#sharelinks.put.edit) |
| [Update Email](actions/update-sharelink-email-by-sharelink-id.md) | `PUT /sharelink/email/:sharelinkId` | [docs](https://api.netexplorer.fr/v3/#sharelinks-email.put.edit) |
| [Update Signature](actions/update-signature-by-signature-id.md) | `PATCH /signature/:signatureId` | [docs](https://api.netexplorer.fr/v3/#signature.patch.update signature) |
| [Update Document](actions/update-signatures-by-signature-id-documents-by-document-id.md) | `PATCH /signatures/:signatureId/documents/:documentId` | [docs](https://api.netexplorer.fr/v3/#signature.patch.update document) |
| [Update Field](actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id.md) | `PATCH /signatures/:signatureId/documents/:documentId/fields/:fieldId` | [docs](https://api.netexplorer.fr/v3/#signature.patch.update field) |
| [Update Category](actions/update-tag-category-by-category-id.md) | `PUT /tag/category/:categoryId` | [docs](https://api.netexplorer.fr/v3/#tags.put.updateCategory) |
| [Update File](actions/update-template-file-by-template-id.md) | `PUT /template/file/:templateId` | [docs](https://api.netexplorer.fr/v3/#template-files.put.update) |
| [Update Trash](actions/update-trash-by-trash-id.md) | `PUT /trash/:trashId` | [docs](https://api.netexplorer.fr/v3/#trash.put.restore) |
| [Update Ulink](actions/update-ulink-by-ulink-id.md) | `PUT /ulink/:ulinkId` | [docs](https://api.netexplorer.fr/v3/#ulinks.put.update) |
| [Update Email](actions/update-ulink-email-by-ulink-email-id.md) | `PUT /ulink/email/:ulinkEmailId` | [docs](https://api.netexplorer.fr/v3/#ulinks-email.put.ulinkEmail) |
| [Update User](actions/update-user-by-user-id.md) | `PUT /user/:userId` | [docs](https://api.netexplorer.fr/v3/#users.put.update) |
