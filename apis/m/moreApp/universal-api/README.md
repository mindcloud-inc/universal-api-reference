# <img src="https://images.mindcloud.co/apps/icons/unnamed-2_1774030146573.png" alt="MoreApp logo" width="28" height="28"> MoreApp: Universal API

MoreApp integration for forms, tasks, files, reports, and webhooks using API key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moreApp/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 90
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://moreapp.com
- **Vendor API docs:** https://docs.moreapp.com/docs/developer-docs/ZG9jOjQ2NDA2-introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Submission File](actions/download-submission-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/download-submission-file?connectionId=$CONNECTION_ID&customerId=1&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (90)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from MoreApp. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves webhook events from MoreApp. |
| [Retrieve Webhook Event](actions/retrieve-webhook-event.md) | GET | Retrieves a webhook event from MoreApp. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes a folder from MoreApp. |
| [Update Folder Property](actions/update-folder-property.md) | PUT | Updates a folder property in MoreApp. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Add Form To Folder](actions/add-form-to-folder.md) | PUT | Adds a form to a folder in MoreApp. |
| [Create Form](actions/create-form.md) | POST | Creates a form in MoreApp. |
| [Create Template](actions/create-template.md) | POST | Creates a template in MoreApp. |
| [Find Forms](actions/find-forms.md) | GET | Finds forms in MoreApp. |
| [Find Templates](actions/find-templates.md) | GET | Finds templates in MoreApp. |
| [Mark Form As Trash](actions/mark-form-as-trash.md) | DELETE | Marks a form as trash in MoreApp. |
| [Mark Template As Trash](actions/mark-template-as-trash.md) | DELETE | Marks a template as trash in MoreApp. |
| [Move Form To Folder](actions/move-form-to-folder.md) | PUT | Moves a form to a folder in MoreApp. |
| [Move Form To Position](actions/move-form-to-position.md) | PUT | Moves a form to a folder position in MoreApp. |
| [Patch Form](actions/patch-form.md) | PUT | Updates specific form properties in MoreApp. |
| [Patch Template](actions/patch-template.md) | PUT | Updates specific template properties in MoreApp. |
| [Remove Form From Folder](actions/remove-form-from-folder.md) | PUT | Removes a form from a folder in MoreApp. |
| [Restore Form To Active](actions/restore-form-to-active.md) | PUT | Restores a form to active in MoreApp. |
| [Restore Template To Active](actions/restore-template-to-active.md) | PUT | Restores a template to active in MoreApp. |
| [Retrieve Form](actions/retrieve-form.md) | GET | Retrieves a form from MoreApp. |
| [Retrieve Template](actions/retrieve-template.md) | GET | Retrieves a template from MoreApp. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | PUT | Adds a user to a group in MoreApp. |
| [Create Group](actions/create-group.md) | POST | Creates a group in MoreApp. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from MoreApp. |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves users in a MoreApp group. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from MoreApp. |
| [Remove User From Group](actions/remove-user-from-group.md) | PUT | Removes a user from a group in MoreApp. |
| [Retrieve Group](actions/retrieve-group.md) | GET | Retrieves a group from MoreApp. |
| [Update Group](actions/update-group.md) | PUT | Updates a group in MoreApp. |
| [Update Group Grant](actions/update-group-grant.md) | PUT | Updates a group's grants in MoreApp. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscriber](actions/create-webhook-subscriber.md) | POST | Creates a webhook subscriber in MoreApp. |
| [Delete Webhook Subscriber](actions/delete-webhook-subscriber.md) | DELETE | Deletes a webhook subscriber from MoreApp. |
| [List Webhook Subscribers](actions/list-webhook-subscribers.md) | GET | Retrieves webhook subscribers from MoreApp. |
| [Retrieve Webhook Subscriber](actions/retrieve-webhook-subscriber.md) | GET | Retrieves a webhook subscriber from MoreApp. |
| [Update Webhook Subscriber](actions/update-webhook-subscriber.md) | PUT | Updates a webhook subscriber in MoreApp. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT | Completes a task in MoreApp. |
| [Create Task](actions/create-task.md) | POST | Creates a task in MoreApp. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from MoreApp. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from MoreApp. |
| [Revoke Task](actions/revoke-task.md) | PUT | Revokes a task in MoreApp. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Invite To Group](actions/add-invite-to-group.md) | PUT |  |
| [Copy Form Version To Folder](actions/copy-form-version-to-folder.md) | PUT | Copies a form version to a folder in MoreApp. |
| [Create Datasource](actions/create-datasource.md) | POST | Creates a datasource in MoreApp. |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in MoreApp. |
| [Create Form Version](actions/create-form-version.md) | POST | Creates a form version in MoreApp. |
| [Create Role](actions/create-role.md) | POST | Creates a role in MoreApp. |
| [Create Template Version](actions/create-template-version.md) | POST |  |
| [Delete Datasource](actions/delete-datasource.md) | DELETE | Deletes a datasource from MoreApp. |
| [Delete Form Version](actions/delete-form-version.md) | DELETE | Deletes a form version from MoreApp. |
| [Delete Role](actions/delete-role.md) | DELETE | Deletes a role from MoreApp. |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes a submission from MoreApp. |
| [Delete Template Version](actions/delete-template-version.md) | DELETE |  |
| [Download Submission File](actions/download-submission-file.md) | GET | Downloads a submission file from MoreApp. |
| [Finalize Form Version](actions/finalize-form-version.md) | PUT | Finalizes a form version for publishing in MoreApp. |
| [Finalize Template Version](actions/finalize-template-version.md) | PUT |  |
| [Get Form Template](actions/get-form-template.md) | GET | Retrieves a form template from MoreApp. |
| [Get Invite Grants](actions/get-invite-grants.md) | GET | Retrieves grants for an invite from MoreApp. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves a submission from MoreApp. |
| [Invite User](actions/invite-user.md) | POST | Invites a user to MoreApp. |
| [List Datasources](actions/list-datasources.md) | GET | Retrieves datasources from MoreApp. |
| [List Exportable Fields](actions/list-exportable-fields.md) | GET | Retrieves exportable submission fields from MoreApp. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from MoreApp. |
| [List Form Versions](actions/list-form-versions.md) | GET | Retrieves form versions from MoreApp. |
| [List Invites](actions/list-invites.md) | GET | Retrieves invites from MoreApp. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from MoreApp. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions from MoreApp. |
| [List Template Versions](actions/list-template-versions.md) | GET | Retrieves template versions from MoreApp. |
| [List Webhook Invocations](actions/list-webhook-invocations.md) | GET | Retrieves webhook invocations from MoreApp. |
| [Remove Invite From Group](actions/remove-invite-from-group.md) | PUT |  |
| [Resend Invite](actions/resend-invite.md) | PUT | Resends an invite in MoreApp. |
| [Resend Submission](actions/resend-submission.md) | PUT | Resends a submission in MoreApp. |
| [Retrieve Datasource](actions/retrieve-datasource.md) | GET | Retrieves a datasource from MoreApp. |
| [Retrieve Folder](actions/retrieve-folder.md) | GET | Retrieves a folder from MoreApp. |
| [Retrieve Form Version](actions/retrieve-form-version.md) | GET | Retrieves a form version from MoreApp. |
| [Retrieve Role](actions/retrieve-role.md) | GET | Retrieves a role from MoreApp. |
| [Retrieve Template Version](actions/retrieve-template-version.md) | GET | Retrieves a template version from MoreApp. |
| [Revoke Invite](actions/revoke-invite.md) | DELETE | Revokes an invite in MoreApp. |
| [Schedule Export](actions/schedule-export.md) | POST | Schedules a submission export in MoreApp. |
| [Update Datasource](actions/update-datasource.md) | PUT | Updates a datasource in MoreApp. |
| [Update Form Version](actions/update-form-version.md) | PUT | Updates a form version in MoreApp. |
| [Update Invite](actions/update-invite.md) | PUT | Updates an invite in MoreApp. |
| [Update Invite Grant](actions/update-invite-grant.md) | PUT | Updates an invite's grants in MoreApp. |
| [Update Role](actions/update-role.md) | PUT | Updates a role in MoreApp. |
| [Update Template Version](actions/update-template-version.md) | PUT |  |
| [Validate Form Version](actions/validate-form-version.md) | PUT | Validates a form version in MoreApp. |
| [Validate Template Version](actions/validate-template-version.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Grants](actions/get-user-grants.md) | GET | Retrieves a user's grants from MoreApp. |
| [List Users](actions/list-users.md) | GET | Retrieves users from MoreApp. |
| [Remove User](actions/remove-user.md) | DELETE | Removes a user from MoreApp. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from MoreApp. |

