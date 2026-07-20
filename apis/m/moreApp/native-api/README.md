# MoreApp: Native API Reference

A consolidated summary of MoreApp's API configuration and 90 documented operations, with links to official documentation.

- **Official docs:** https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction
- **API base URL:** `https://api.moreapp.com`

## Authentication

### API Key (Header Only)

Connect MoreApp using an API key sent only in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · optional · MoreApp API key used for X-Api-Key request headers.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.moreapp.com/docs/developer-docs/b6b6c2d4906e9-authentication)

## Endpoints (90 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Form To Folder](actions/add-form-to-folder.md) | `POST /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/d057b1cf39424-add-form-to-folder) |
| [Add Invite To Group](actions/add-invite-to-group.md) | `POST /api/v2/customers/{{customerId}}/invites/{{inviteId}}/groups/{{groupId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction) |
| [Add User To Group](actions/add-user-to-group.md) | `POST /api/v2/customers/{{customerId}}/groups/{{groupId}}/users/{{userId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/81d814eeaa125-add-user-to-group) |
| [Complete Task](actions/complete-task.md) | `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}/complete` | [docs](https://docs.moreapp.com/docs/developer-docs/56175a9cab2d8-complete-a-task) |
| [Copy Form Version To Folder](actions/copy-form-version-to-folder.md) | `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/copy` | [docs](https://docs.moreapp.com/docs/developer-docs/21958495a97bc-copy-form-version-to-specified-folder) |
| [Create Datasource](actions/create-datasource.md) | `POST /api/v1.0/customers/{{customerId}}/datasources` | [docs](https://docs.moreapp.com/docs/developer-docs/5c7a4e7b26a0e-create-a-datasource) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1.0/forms/customer/{{customerId}}/folders` | [docs](https://docs.moreapp.com/docs/developer-docs/08e73bcc90173-create-folder) |
| [Create Form](actions/create-form.md) | `POST /api/v1.0/forms/customer/{{customerId}}/forms` | [docs](https://docs.moreapp.com/docs/developer-docs/e2adf91c4478e-create-form) |
| [Create Form Version](actions/create-form-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions` | [docs](https://docs.moreapp.com/docs/developer-docs/52fae54761987-create-form-version) |
| [Create Group](actions/create-group.md) | `POST /api/v2/customers/{{customerId}}/groups` | [docs](https://docs.moreapp.com/docs/developer-docs/9a2a824bacb05-create-group) |
| [Create Role](actions/create-role.md) | `POST /api/v2/customers/{{customerId}}/roles` | [docs](https://docs.moreapp.com/docs/developer-docs/da466a2b39bb2-create-role) |
| [Create Task](actions/create-task.md) | `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks` | [docs](https://docs.moreapp.com/docs/developer-docs/657b678d8ad54-create-a-task) |
| [Create Template](actions/create-template.md) | `POST /api/v1.0/forms/customer/{{customerId}}/templates` | [docs](https://docs.moreapp.com/docs/developer-docs/14b8ea3c3ed4f-create-template) |
| [Create Template Version](actions/create-template-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions` | [docs](https://docs.moreapp.com/docs/developer-docs/a10fa9e66b164-get-versions-of-a-template) |
| [Create Webhook Subscriber](actions/create-webhook-subscriber.md) | `POST /api/v1.0/webhooks/customer/{{customerId}}/subscribers` | [docs](https://docs.moreapp.com/docs/developer-docs/fea134e0e69b2-create-a-subscriber) |
| [Delete Datasource](actions/delete-datasource.md) | `DELETE /api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/a3de527c2edad-delete-a-datasource) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/9a1c7d0abb95e-delete-folder) |
| [Delete Form Version](actions/delete-form-version.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8bb61d4e4461b-delete-form-version) |
| [Delete Group](actions/delete-group.md) | `DELETE /api/v2/customers/{{customerId}}/groups/{{groupId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/149735c9e7cdc-delete-group) |
| [Delete Role](actions/delete-role.md) | `DELETE /api/v2/customers/{{customerId}}/roles/{{roleId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/a7b42a27490bf-delete-role) |
| [Delete Submission](actions/delete-submission.md) | `DELETE /api/v1.0/customers/{{customerId}}/submissions/{{submissionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/b9bd9cc2b74ef-delete-a-submission) |
| [Delete Template Version](actions/delete-template-version.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8323e40d67523-get-a-specific-version-of-a-template) |
| [Delete Webhook Subscriber](actions/delete-webhook-subscriber.md) | `DELETE /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/1dcc9c1c7b668-delete-a-subscriber) |
| [Download Submission File](actions/download-submission-file.md) | `GET /api/v1.0/customers/{{customerId}}/registrationFile/{{fileId}}/download` | [docs](https://docs.moreapp.com/docs/developer-docs/ce7e32b88411a-download-submission-file) |
| [Finalize Form Version](actions/finalize-form-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}/finalize` | [docs](https://docs.moreapp.com/docs/developer-docs/7a8379cd18397-finalize-for-publish-form-version) |
| [Finalize Template Version](actions/finalize-template-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}/finalize` | [docs](https://docs.moreapp.com/docs/developer-docs/8323e40d67523-get-a-specific-version-of-a-template) |
| [Find Forms](actions/find-forms.md) | `GET /api/v1.0/forms/customer/{{customerId}}/forms` | [docs](https://docs.moreapp.com/docs/developer-docs/c942f242b1b97-find-forms) |
| [Find Templates](actions/find-templates.md) | `GET /api/v1.0/forms/customer/{{customerId}}/templates` | [docs](https://docs.moreapp.com/docs/developer-docs/0d2f747ca6fa8-find-templates) |
| [Get Form Template](actions/get-form-template.md) | `GET /api/v1.0/forms/customer/{{customerId}}/forms/templates/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/6f629f56cb4be-get-a-form-template) |
| [Get Invite Grants](actions/get-invite-grants.md) | `GET /api/v2/customers/{{customerId}}/invites/{{id}}/grants` | [docs](https://docs.moreapp.com/docs/developer-docs/9606bfeae6e60-get-grants-for-invite) |
| [Get Submission](actions/get-submission.md) | `GET /api/v1.0/customers/{{customerId}}/submissions/{{submissionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/42c8ecbd569f3-get-a-single-submission) |
| [Get User Grants](actions/get-user-grants.md) | `GET /api/v2/customers/{{customerId}}/users/{{userId}}/grants` | [docs](https://docs.moreapp.com/docs/developer-docs/3bd1645996df5-get-grants-for-user) |
| [Invite User](actions/invite-user.md) | `POST /api/v2/customers/{{customerId}}/invites` | [docs](https://docs.moreapp.com/docs/developer-docs/b91036c4f16dd-invite-user) |
| [List Datasources](actions/list-datasources.md) | `GET /api/v1.0/customers/{{customerId}}/datasources` | [docs](https://docs.moreapp.com/docs/developer-docs/3eb7f77868583-list-all-datasources) |
| [List Exportable Fields](actions/list-exportable-fields.md) | `GET /api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export/fields` | [docs](https://docs.moreapp.com/docs/developer-docs/5eb67d5bdcd81-list-all-exportable-fields) |
| [List Folders](actions/list-folders.md) | `GET /api/v1.0/forms/customer/{{customerId}}/folders` | [docs](https://docs.moreapp.com/docs/developer-docs/4627bd66fda96-get-available-folders-for-customer) |
| [List Form Versions](actions/list-form-versions.md) | `GET /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions` | [docs](https://docs.moreapp.com/docs/developer-docs/d731a224934e1-get-versions-of-a-form) |
| [List Group Users](actions/list-group-users.md) | `GET /api/v2/customers/{{customerId}}/groups/{{groupId}}/users` | [docs](https://docs.moreapp.com/docs/developer-docs/af4728fa7f56c-list-users-within-group) |
| [List Groups](actions/list-groups.md) | `GET /api/v2/customers/{{customerId}}/groups` | [docs](https://docs.moreapp.com/docs/developer-docs/2734967502d3e-list-all-groups) |
| [List Invites](actions/list-invites.md) | `GET /api/v2/customers/{{customerId}}/invites` | [docs](https://docs.moreapp.com/docs/developer-docs/5e8fe257ca978-list-all-invites) |
| [List Roles](actions/list-roles.md) | `GET /api/v2/customers/{{customerId}}/roles` | [docs](https://docs.moreapp.com/docs/developer-docs/41b7fc48e3872-get-roles-for-account) |
| [List Submissions](actions/list-submissions.md) | `POST /api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/filter/{{page}}` | [docs](https://docs.moreapp.com/docs/developer-docs/9a6201b9c0c73-list-all-submissions) |
| [List Tasks](actions/list-tasks.md) | `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/filter/{{page}}` | [docs](https://docs.moreapp.com/docs/developer-docs/e1305a3576723-list-all-tasks) |
| [List Template Versions](actions/list-template-versions.md) | `GET /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions` | [docs](https://docs.moreapp.com/docs/developer-docs/a10fa9e66b164-get-versions-of-a-template) |
| [List Users](actions/list-users.md) | `GET /api/v1.0/customers/{{customerId}}/users` | [docs](https://docs.moreapp.com/docs/developer-docs/1050875ee7b7d-list-all-users) |
| [List Webhook Events](actions/list-webhook-events.md) | `GET /api/v1.0/webhooks/customer/{{customerId}}/events` | [docs](https://docs.moreapp.com/docs/developer-docs/4e9b52015e45f-list-all-events) |
| [List Webhook Invocations](actions/list-webhook-invocations.md) | `GET /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}/invocations` | [docs](https://docs.moreapp.com/docs/developer-docs/92dd591d20e9b-list-all-invocations) |
| [List Webhook Subscribers](actions/list-webhook-subscribers.md) | `GET /api/v1.0/webhooks/customer/{{customerId}}/subscribers` | [docs](https://docs.moreapp.com/docs/developer-docs/fe9894cd0a286-list-all-subscribers) |
| [Mark Form As Trash](actions/mark-form-as-trash.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/c3ee85a1f570b-mark-form-as-trash) |
| [Mark Template As Trash](actions/mark-template-as-trash.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/ab3f447dabd14-mark-template-as-trash) |
| [Move Form To Folder](actions/move-form-to-folder.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/47e79e1f60727-move-form-to-folder) |
| [Move Form To Position](actions/move-form-to-position.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}/move/{{position}}` | [docs](https://docs.moreapp.com/docs/developer-docs/01a23351e14db-move-form-to-specific-position-in-folder) |
| [Patch Form](actions/patch-form.md) | `PATCH /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/fa28120e4d482-patch-specific-property-of-form) |
| [Patch Template](actions/patch-template.md) | `PATCH /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/049ea5e5cf21c-patch-specific-property-of-a-template) |
| [Remove Form From Folder](actions/remove-form-from-folder.md) | `DELETE /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/982e234d5b352-remove-form-from-folder) |
| [Remove Invite From Group](actions/remove-invite-from-group.md) | `DELETE /api/v2/customers/{{customerId}}/invites/{{inviteId}}/groups/{{groupId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction) |
| [Remove User](actions/remove-user.md) | `DELETE /api/v1.0/customers/{{customerId}}/users/{{userId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/c6474802fa5c1-remove-a-user) |
| [Remove User From Group](actions/remove-user-from-group.md) | `DELETE /api/v2/customers/{{customerId}}/groups/{{groupId}}/users/{{userId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/fb988900981f1-remove-user-from-group) |
| [Resend Invite](actions/resend-invite.md) | `GET /api/v2/customers/{{customerId}}/invites/{{id}}/resend` | [docs](https://docs.moreapp.com/docs/developer-docs/7d1ef261253f6-resend-invite) |
| [Resend Submission](actions/resend-submission.md) | `PUT /api/v1.0/customers/{{customerId}}/submissions/resend/{{submissionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/1df53b019ea65-resend-a-submission) |
| [Restore Form To Active](actions/restore-form-to-active.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/741525e8ed9a4-restore-form-to-active) |
| [Restore Template To Active](actions/restore-template-to-active.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8e45a4386d0e8-restore-template-to-active) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /api/v1.0/customers/{{customerId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/97fdccb79c39d-retrieve-a-customer) |
| [Retrieve Datasource](actions/retrieve-datasource.md) | `GET /api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/1d826aa0c516a-retrieve-a-datasource) |
| [Retrieve Folder](actions/retrieve-folder.md) | `GET /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/2bce680f6a839-get-folder) |
| [Retrieve Form](actions/retrieve-form.md) | `GET /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/269963b4a5c3d-get-form) |
| [Retrieve Form Version](actions/retrieve-form-version.md) | `GET /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/0b97f381e2f71-get-a-specific-version-of-a-form) |
| [Retrieve Group](actions/retrieve-group.md) | `GET /api/v2/customers/{{customerId}}/groups/{{groupId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/b747d3ac1da61-retrieve-a-group) |
| [Retrieve Role](actions/retrieve-role.md) | `GET /api/v2/customers/{{customerId}}/roles/{{roleId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/2336cb776f390-retrieve-a-role) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/a2c30297eb5a8-retrieve-a-task) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/68a89bcf059f6-get-template) |
| [Retrieve Template Version](actions/retrieve-template-version.md) | `GET /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8323e40d67523-get-a-specific-version-of-a-template) |
| [Retrieve User](actions/retrieve-user.md) | `GET /api/v1.0/customers/{{customerId}}/users/{{userId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/504d734002123-retrieve-a-user) |
| [Retrieve Webhook Event](actions/retrieve-webhook-event.md) | `GET /api/v1.0/webhooks/customer/{{customerId}}/events/{{eventId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/d69445f35889b-retrieve-an-event) |
| [Retrieve Webhook Subscriber](actions/retrieve-webhook-subscriber.md) | `GET /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/07bc433ed2ba5-retrieve-a-subscriber) |
| [Revoke Invite](actions/revoke-invite.md) | `DELETE /api/v2/customers/{{customerId}}/invites/{{id}}` | [docs](https://docs.moreapp.com/docs/developer-docs/d33c664a81b0b-revoke-invite) |
| [Revoke Task](actions/revoke-task.md) | `POST /api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}/revoke` | [docs](https://docs.moreapp.com/docs/developer-docs/41a7f9dc561ff-revoke-a-task) |
| [Schedule Export](actions/schedule-export.md) | `POST /api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export` | [docs](https://docs.moreapp.com/docs/developer-docs/45b37124ae038-schedule-an-export) |
| [Update Datasource](actions/update-datasource.md) | `PUT /api/v1.0/customers/{{customerId}}/datasources/{{dataSourceId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/52b1fb0c9b961-update-a-datasource) |
| [Update Folder Property](actions/update-folder-property.md) | `PATCH /api/v1.0/forms/customer/{{customerId}}/folders/{{folderId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8a56cc803116b-update-property-of-folder) |
| [Update Form Version](actions/update-form-version.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/6e4778ea3dc32-update-form-version) |
| [Update Group](actions/update-group.md) | `PATCH /api/v2/customers/{{customerId}}/groups/{{groupId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/dd580afded7b4-modify-group) |
| [Update Group Grant](actions/update-group-grant.md) | `PATCH /api/v2/customers/{{customerId}}/groups/{{groupId}}/grants` | [docs](https://docs.moreapp.com/docs/developer-docs/9f16580180528-add-remove-grant) |
| [Update Invite](actions/update-invite.md) | `PUT /api/v2/customers/{{customerId}}/invites/{{id}}` | [docs](https://docs.moreapp.com/docs/developer-docs/3da3bf74dfc23-update-invite) |
| [Update Invite Grant](actions/update-invite-grant.md) | `PATCH /api/v2/customers/{{customerId}}/invites/{{id}}/grants` | [docs](https://docs.moreapp.com/docs/developer-docs/180b38f242fc7-add-update-remove-grant) |
| [Update Role](actions/update-role.md) | `PATCH /api/v2/customers/{{customerId}}/roles/{{roleId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/2bda39e46b7a6-modify-role) |
| [Update Template Version](actions/update-template-version.md) | `PUT /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/{{formVersionId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/8323e40d67523-get-a-specific-version-of-a-template) |
| [Update Webhook Subscriber](actions/update-webhook-subscriber.md) | `PUT /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}` | [docs](https://docs.moreapp.com/docs/developer-docs/fb9dac850ba59-update-a-subscriber) |
| [Validate Form Version](actions/validate-form-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/forms/{{formId}}/versions/validate` | [docs](https://docs.moreapp.com/docs/developer-docs/0e8bad70e535a-validate-form-version) |
| [Validate Template Version](actions/validate-template-version.md) | `POST /api/v1.0/forms/customer/{{customerId}}/templates/{{formId}}/versions/validate` | [docs](https://docs.moreapp.com/docs/developer-docs/a10fa9e66b164-get-versions-of-a-template) |
