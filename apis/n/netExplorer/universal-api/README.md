# <img src="https://images.mindcloud.co/apps/icons/net-explorer_1775659117820.png" alt="NetExplorer logo" width="28" height="28"> NetExplorer: Universal API

Secure cloud file storage and collaboration for NetExplorer tenants, including folders, files, shares, upload links, archives, locks, and trash workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/netExplorer/latest
- **Category:** Content & Files / Storage
- **Actions:** 240
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://netexplorer.fr
- **Vendor API docs:** https://api.netexplorer.fr/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (240)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Update Account Picture](actions/create-account-picture.md) | POST |  |
| [Reset Password](actions/create-reset-password.md) | POST |  |
| [Delete Account Picture](actions/delete-account-picture.md) | DELETE |  |
| [Get Account](actions/get-account.md) | GET |  |
| [Get Account Picture](actions/get-account-picture.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List File Activity](actions/get-activity-file-by-file-id.md) | GET |  |
| [List Folder Activity](actions/get-activity-folder-by-folder-id.md) | GET |  |

### Admin

| Action | Method | Description |
| --- | --- | --- |
| [Get Fzen](actions/get-fzen.md) | GET |  |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert](actions/create-alert.md) | POST |  |
| [Delete Alert](actions/delete-alert-by-alert-id.md) | DELETE |  |
| [Get Alert By Alert ID](actions/get-alert-by-alert-id.md) | GET |  |
| [List Alerts](actions/get-alerts-by-folder-id.md) | GET |  |
| [Update Alert](actions/update-alert-by-alert-id.md) | PUT |  |

### Annotations

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST |  |
| [Delete Annotation](actions/delete-annotation-by-annotation-id.md) | DELETE |  |
| [Get Annotation By Annotation ID](actions/get-annotation-by-annotation-id.md) | GET |  |
| [Get All](actions/get-annotations-all.md) | GET |  |
| [List Annotations](actions/get-annotations-by-target-id-by-type.md) | GET |  |
| [Update Annotation](actions/update-annotation-by-annotation-id.md) | PUT |  |
| [Update All](actions/update-annotations-all.md) | PUT |  |

### Archive

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-archive-folder.md) | POST |  |
| [Delete File](actions/delete-archive-file-by-file-id.md) | DELETE |  |
| [Delete Folder](actions/delete-archive-folder-by-folder-id.md) | DELETE |  |
| [Get File](actions/get-archive-file-by-file-id.md) | GET |  |
| [Get Folder](actions/get-archive-folder-by-folder-id.md) | GET |  |
| [Update File](actions/update-archive-file-by-file-id.md) | PUT |  |
| [Unarchive File](actions/update-archive-file-by-file-id-unarchive.md) | PUT |  |
| [Update Folder](actions/update-archive-folder-by-folder-id.md) | PUT |  |
| [Unarchive Folder](actions/update-archive-folder-by-folder-id-unarchive.md) | PUT |  |
| [Archive File](actions/update-file-by-file-id-archive.md) | PUT |  |
| [Archive Folder](actions/update-folder-by-folder-id-archive.md) | PUT |  |

### Config

| Action | Method | Description |
| --- | --- | --- |
| [Create Test](actions/create-config-smtp-test.md) | POST |  |
| [Get Config](actions/get-config.md) | GET |  |
| [Get Publicconfig](actions/get-publicconfig.md) | GET |  |
| [Update Config](actions/update-config.md) | PUT |  |

### Delegates

| Action | Method | Description |
| --- | --- | --- |
| [Create Delegate](actions/create-delegate.md) | POST |  |
| [Delete Delegate](actions/delete-delegate-by-delegate-id.md) | DELETE |  |
| [Get Delegate By Delegate ID](actions/get-delegate-by-delegate-id.md) | GET |  |
| [List Delegates](actions/get-delegates-by-group-id.md) | GET |  |
| [Update Delegate](actions/update-delegate-by-delegate-id.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-email.md) | POST |  |
| [Delete Email](actions/delete-email-by-email-id.md) | DELETE |  |
| [Get Email By Email ID](actions/get-email-by-email-id.md) | GET |  |
| [List Emails](actions/get-emails.md) | GET |  |
| [Update Email](actions/update-email-by-email-id.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |
| [Create Tus Upload](actions/create-file-tus.md) | POST |  |
| [Upload File](actions/create-file-upload.md) | POST |  |
| [Delete File](actions/delete-file-by-file-id.md) | DELETE |  |
| [Cancel File Upload](actions/delete-file-cancel.md) | DELETE |  |
| [Get Activity](actions/get-file-activity.md) | GET |  |
| [Get File By File ID](actions/get-file-by-file-id.md) | GET |  |
| [Download File By File ID](actions/get-file-by-file-id-download.md) | GET |  |
| [Get File Info](actions/get-file-by-file-id-infos.md) | GET |  |
| [Get File Timeline](actions/get-file-by-file-id-timeline.md) | GET |  |
| [List File Versions](actions/get-file-by-file-id-versions.md) | GET |  |
| [Download File](actions/get-file-download.md) | GET |  |
| [Update File](actions/update-file-by-file-id.md) | PUT |  |
| [Update File Upload](actions/update-file-by-fileid-upload.md) | PUT |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder-by-folder-id.md) | DELETE |  |
| [Get Folder By Folder ID](actions/get-folder-by-folder-id.md) | GET |  |
| [Get Folder Timeline](actions/get-folder-by-folder-id-timeline.md) | GET |  |
| [List Folders](actions/get-folders.md) | GET |  |
| [Update Folder](actions/update-folder-by-folder-id.md) | PUT |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST |  |
| [Delete Group](actions/delete-group-by-group-id.md) | DELETE |  |
| [Get Group By Group ID](actions/get-group-by-group-id.md) | GET |  |
| [List Groups](actions/get-groups.md) | GET |  |
| [Update Group](actions/update-group-by-group-id.md) | PUT |  |

### Identity

| Action | Method | Description |
| --- | --- | --- |
| [Create Provider](actions/create-identity-provider.md) | POST |  |
| [Create Sync](actions/create-identity-provider-by-id-sync.md) | POST |  |
| [Create Test](actions/create-identity-provider-test.md) | POST |  |
| [Delete Provider](actions/delete-identity-provider-by-id.md) | DELETE |  |
| [Get Provider](actions/get-identity-provider-by-id.md) | GET |  |
| [Get Matching](actions/get-identity-provider-by-id-matching.md) | GET |  |
| [Get Provider](actions/get-identity-providers.md) | GET |  |
| [Update Provider](actions/update-identity-provider-by-id.md) | PUT |  |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Create Invite](actions/create-invite.md) | POST |  |
| [Delete Invite](actions/delete-invite-by-invite-id.md) | DELETE |  |
| [Get User](actions/get-invite-users-by-folder-id.md) | GET |  |
| [List Invites](actions/get-invites-by-folder-id.md) | GET |  |
| [Update Invite](actions/update-invite-by-invitation-id.md) | PUT |  |

### Locks

| Action | Method | Description |
| --- | --- | --- |
| [Delete Lock](actions/delete-lock-by-file-id.md) | DELETE |  |
| [Get Lock By File ID](actions/get-lock-by-file-id.md) | GET |  |
| [List Locks](actions/get-locks-by-folder-id.md) | GET |  |
| [Update Lock](actions/update-lock-by-file-id.md) | PUT |  |

### Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Log By Log ID](actions/get-log-by-log-id.md) | GET |  |
| [List Logs](actions/get-logs.md) | GET |  |

### Oauth2 Applications

| Action | Method | Description |
| --- | --- | --- |
| [Create App](actions/create-oauth2-app.md) | POST |  |
| [Reset App Secret](actions/create-oauth2-app-by-client-id-reset.md) | POST |  |
| [Delete App](actions/delete-oauth2-app-by-client-id.md) | DELETE |  |
| [Revoke App](actions/delete-oauth2-app-by-token-revoke.md) | DELETE |  |
| [Revoke User](actions/delete-oauth2-user-by-token-revoke.md) | DELETE |  |
| [Get App](actions/get-oauth2-app-by-client-id.md) | GET |  |
| [Get Icon](actions/get-oauth2-app-by-client-id-icon.md) | GET |  |
| [Get Token](actions/get-oauth2-app-by-client-id-tokens.md) | GET |  |
| [Get App](actions/get-oauth2-apps.md) | GET |  |
| [Get Token](actions/get-oauth2-user-tokens.md) | GET |  |
| [Update App](actions/update-oauth2-app-by-client-id.md) | PUT |  |

### Options

| Action | Method | Description |
| --- | --- | --- |
| [Delete Option](actions/delete-option-by-user-id.md) | DELETE |  |
| [Get Option By User ID](actions/get-option-by-user-id.md) | GET |  |
| [Update Option](actions/update-option-by-user-id.md) | PUT |  |

### Preview

| Action | Method | Description |
| --- | --- | --- |
| [Get Mixer By File ID](actions/get-mixer-by-file-id.md) | GET |  |
| [Get Preview By File ID](actions/get-preview-by-file-id.md) | GET |  |

### Rights

| Action | Method | Description |
| --- | --- | --- |
| [Create Right](actions/create-right.md) | POST |  |
| [Delete Right](actions/delete-right-by-right-id.md) | DELETE |  |
| [Get Right By Right ID](actions/get-right-by-right-id.md) | GET |  |
| [List Rights](actions/get-rights-by-folder-id.md) | GET |  |
| [Update Right](actions/update-right-by-right-id.md) | PUT |  |

### Roots

| Action | Method | Description |
| --- | --- | --- |
| [Get Root By Type](actions/get-root-by-type.md) | GET |  |
| [Get Portal Root](actions/get-root-portal-by-filter.md) | GET |  |
| [List Roots](actions/get-roots.md) | GET |  |

### Share Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-share-email.md) | POST |  |
| [Delete Email](actions/delete-share-email-by-share-email-id.md) | DELETE |  |
| [Get Email](actions/get-share-email-by-share-email-id.md) | GET |  |
| [Get Activity](actions/get-share-email-by-share-email-id-activity.md) | GET |  |
| [Get Email](actions/get-shares-emails.md) | GET |  |
| [Update Email](actions/update-share-email-by-share-email-id.md) | PUT |  |

### Sharelink Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-sharelink-email.md) | POST |  |
| [Delete Email](actions/delete-sharelink-email-by-sharelink-email-id.md) | DELETE |  |
| [Get Email](actions/get-sharelink-email-by-sharelink-email-id.md) | GET |  |
| [Get Email](actions/get-sharelinks-emails.md) | GET |  |
| [Update Email](actions/update-sharelink-email-by-sharelink-id.md) | PUT |  |

### Sharelinks

| Action | Method | Description |
| --- | --- | --- |
| [Create Sharelink](actions/create-sharelink.md) | POST |  |
| [Create File](actions/create-sharelink-by-sharelink-id-file.md) | POST |  |
| [Create Folder](actions/create-sharelink-by-sharelink-id-folder.md) | POST |  |
| [Validate Sharelink Password](actions/create-sharelink-by-sharelink-id-passcheck.md) | POST |  |
| [Validate Sharelink Password](actions/create-sharelink-key-by-sharelink-key-passcheck.md) | POST |  |
| [Delete Sharelink](actions/delete-sharelink-by-sharelink-id.md) | DELETE |  |
| [Delete File](actions/delete-sharelink-by-sharelink-id-file-by-file-id.md) | DELETE |  |
| [Get Sharelink By Sharelink ID](actions/get-sharelink-by-sharelink-id.md) | GET |  |
| [Download Sharelink By Sharelink Key](actions/get-sharelink-download-by-sharelink-key.md) | GET |  |
| [Get Key](actions/get-sharelink-key-by-sharelink-key.md) | GET |  |
| [List Sharelinks](actions/get-sharelinks.md) | GET |  |
| [Update Sharelink](actions/update-sharelink-by-sharelink-id.md) | PUT |  |

### Shares

| Action | Method | Description |
| --- | --- | --- |
| [Create Share](actions/create-share.md) | POST |  |
| [Validate Sharelink Password](actions/create-share-key-by-share-key-passcheck.md) | POST |  |
| [Send Share SMS](actions/create-share-key-by-share-key-sms.md) | POST |  |
| [Create Share](actions/create-zip-token-share.md) | POST |  |
| [Delete Share](actions/delete-share-by-share-id.md) | DELETE |  |
| [Get Share By Share ID](actions/get-share-by-share-id.md) | GET |  |
| [Get Activity](actions/get-share-by-share-id-activity.md) | GET |  |
| [Get Share Content](actions/get-share-content-by-share-key-folder-id.md) | GET |  |
| [Get File](actions/get-share-download-file.md) | GET |  |
| [Get Key](actions/get-share-key-by-share-key.md) | GET |  |
| [List Shares](actions/get-shares.md) | GET |  |
| [Get Share](actions/get-zip-share-by-share-key.md) | GET |  |
| [Update Share](actions/update-share-by-share-id.md) | PUT |  |

### Signature

| Action | Method | Description |
| --- | --- | --- |
| [Create Signature](actions/create-signatures.md) | POST |  |
| [Create Activate](actions/create-signatures-by-signature-id-activate.md) | POST |  |
| [Create Actor](actions/create-signatures-by-signature-id-actors.md) | POST |  |
| [Create Remind](actions/create-signatures-by-signature-id-actors-by-actor-id-remind.md) | POST |  |
| [Create Remind](actions/create-signatures-by-signature-id-actors-remind.md) | POST |  |
| [Create Cancel](actions/create-signatures-by-signature-id-cancel.md) | POST |  |
| [Create Field](actions/create-signatures-by-signature-id-documents-by-document-id-fields.md) | POST |  |
| [Create Document](actions/create-signatures-by-signature-id-documents-by-file-id.md) | POST |  |
| [Delete Signature](actions/delete-signatures-by-signature-id.md) | DELETE |  |
| [Delete Actor](actions/delete-signatures-by-signature-id-actors-by-actor-id.md) | DELETE |  |
| [Delete Document](actions/delete-signatures-by-signature-id-documents-by-document-id.md) | DELETE |  |
| [Delete Signature Field](actions/delete-signatures-by-signature-id-documents-by-document-id-fields-field-id.md) | DELETE |  |
| [List Signatures](actions/get-signatures.md) | GET |  |
| [List Signatures](actions/get-signatures-by-signature-id.md) | GET |  |
| [Get Activity](actions/get-signatures-by-signature-id-activities.md) | GET |  |
| [Get Export](actions/get-signatures-by-signature-id-activities-export.md) | GET |  |
| [Get Audit](actions/get-signatures-by-signature-id-actors-audit.md) | GET |  |
| [Get Audit](actions/get-signatures-by-signature-id-actors-by-actor-id-audit.md) | GET |  |
| [Get Signed](actions/get-signatures-by-signature-id-documents-by-document-id-signed.md) | GET |  |
| [Get Signed](actions/get-signatures-by-signature-id-documents-signed.md) | GET |  |
| [Get Export](actions/get-signatures-export.md) | GET |  |
| [Get Received](actions/get-signatures-received.md) | GET |  |
| [Get Export](actions/get-signatures-received-export.md) | GET |  |
| [Update Signature](actions/update-signature-by-signature-id.md) | PUT |  |
| [Update Document](actions/update-signatures-by-signature-id-documents-by-document-id.md) | PUT |  |
| [Update Field](actions/update-signatures-by-signature-id-documents-by-document-id-fields-by-field-id.md) | PUT |  |

### Sync

| Action | Method | Description |
| --- | --- | --- |
| [Get Ischildof](actions/get-ischildof.md) | GET |  |
| [Get Objectpath](actions/get-objectpath.md) | GET |  |
| [Get Path](actions/get-path.md) | GET |  |
| [List Quotas](actions/get-quotas.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Create Folder](actions/create-tag-by-folder-id-folder.md) | POST |  |
| [Create Tag](actions/create-tag-by-tag-id-by-element-id-by-type.md) | POST |  |
| [Create Category](actions/create-tag-category.md) | POST |  |
| [Delete Tag](actions/delete-tag-by-tag-id.md) | DELETE |  |
| [Delete Tag](actions/delete-tag-by-tag-id-by-element-id-by-type.md) | DELETE |  |
| [Delete Category](actions/delete-tag-category-by-category-id.md) | DELETE |  |
| [Get Tag By Tag ID](actions/get-tag-by-tag-id.md) | GET |  |
| [Get Category](actions/get-tag-categories.md) | GET |  |
| [Get Attached](actions/get-tag-categories-attached-by-element-id-by-type.md) | GET |  |
| [Get Category](actions/get-tag-categories-by-element-id-by-type.md) | GET |  |
| [Get Category](actions/get-tag-category-by-category-id.md) | GET |  |
| [Get Category](actions/get-tag-category-by-category-id-by-element-id-by-type.md) | GET |  |
| [List Tags](actions/get-tags.md) | GET |  |
| [Get Color](actions/get-tags-colors.md) | GET |  |
| [Update Category](actions/update-tag-category-by-category-id.md) | PUT |  |

### Template Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-template-file.md) | POST |  |
| [Copy Template File](actions/create-template-file-copy.md) | POST |  |
| [Delete File](actions/delete-template-file-by-template-id.md) | DELETE |  |
| [List Template Files](actions/get-template-files-by-folder-id.md) | GET |  |
| [Get Template Folder](actions/get-template-folder.md) | GET |  |
| [Update File](actions/update-template-file-by-template-id.md) | PUT |  |

### Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Generate Token Token](actions/create-token-file-by-file-id-by-type.md) | POST |  |
| [Generate Token Token](actions/create-token-share-by-guid-by-type-by-key.md) | POST |  |
| [Generate Share Download Token](actions/create-token-share-download-by-key.md) | POST |  |
| [Generate Token Token](actions/create-token-sharelink-by-key-by-data-id-by-type.md) | POST |  |
| [Generate Sharelink Download Token](actions/create-token-sharelink-by-key-download.md) | POST |  |
| [Generate Token Token](actions/create-token-template-by-id-by-type.md) | POST |  |

### Trash

| Action | Method | Description |
| --- | --- | --- |
| [Delete Trash](actions/delete-trash-by-trash-id.md) | DELETE |  |
| [Delete Trashe](actions/delete-trashes.md) | DELETE |  |
| [Get Trash By Trash ID](actions/get-trash-by-trash-id.md) | GET |  |
| [List Trashes](actions/get-trashes.md) | GET |  |
| [Update Trash](actions/update-trash-by-trash-id.md) | PUT |  |

### Upload Link Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Email](actions/create-ulink-email.md) | POST |  |
| [Delete Email](actions/delete-ulink-email-by-ulink-email-id.md) | DELETE |  |
| [Get Email](actions/get-ulink-email-by-ulink-email-id.md) | GET |  |
| [Get Email](actions/get-ulinks-emails.md) | GET |  |
| [Update Email](actions/update-ulink-email-by-ulink-email-id.md) | PUT |  |

### Upload Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Ulink](actions/create-ulink.md) | POST |  |
| [Validate Sharelink Password](actions/create-ulink-key-by-ulink-key-passcheck.md) | POST |  |
| [Send Upload Link SMS](actions/create-ulink-key-by-ulink-key-sms.md) | POST |  |
| [Delete Ulink](actions/delete-ulink-by-ulink-id.md) | DELETE |  |
| [Get Ulink By Ulink ID](actions/get-ulink-by-ulink-id.md) | GET |  |
| [Get Key](actions/get-ulink-key-by-ulink-key.md) | GET |  |
| [List Ulinks](actions/get-ulinks.md) | GET |  |
| [Update Ulink](actions/update-ulink-by-ulink-id.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Update User Picture](actions/create-user-by-user-id-picture.md) | POST |  |
| [Delete User](actions/delete-user-by-user-id.md) | DELETE |  |
| [Delete User Picture](actions/delete-user-by-user-id-picture.md) | DELETE |  |
| [Get User By User ID](actions/get-user-by-user-id.md) | GET |  |
| [Get User Picture](actions/get-user-by-user-id-picture.md) | GET |  |
| [Get User Quota](actions/get-user-by-user-id-quota.md) | GET |  |
| [List Users](actions/get-users.md) | GET |  |
| [Update User](actions/update-user-by-user-id.md) | PUT |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Instance](actions/create-workflow-instance.md) | POST |  |
| [Delete Instance](actions/delete-workflow-instance-by-instance-id.md) | DELETE |  |
| [Get Instance](actions/get-workflow-instance-by-token.md) | GET |  |
| [Get Instance](actions/get-workflow-instances.md) | GET |  |

### Zip

| Action | Method | Description |
| --- | --- | --- |
| [Get Zip](actions/get-zip.md) | GET |  |

