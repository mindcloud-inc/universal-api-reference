# <img src="https://images.mindcloud.co/apps/icons/opn-form_1774467639959.png" alt="OpnForm logo" width="28" height="28"> OpnForm: Universal API

Create and manage forms, submissions, workspaces, and members

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/opnForm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opnform.com
- **Vendor API docs:** https://docs.opnform.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Check Submission Export Status](actions/check-submission-export-status.md) | GET | Retrieves submission export job status from OpnForm. |
| [Export Submissions CSV](actions/export-submissions-csv.md) | GET | Exports form submissions as CSV from OpnForm. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | DELETE | Deletes an existing submission from OpnForm. |
| [List Submissions](actions/list-submissions.md) | GET | Lists submissions for an OpnForm form. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in OpnForm. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in OpnForm. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from OpnForm. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from OpnForm by slug. |
| [List Workspace Forms](actions/list-workspace-forms.md) | GET | Lists forms in an OpnForm workspace. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in OpnForm. |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Integration](actions/create-webhook-integration.md) | POST | Creates a webhook integration in OpnForm. |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | DELETE | Deletes an existing webhook integration from OpnForm. |
| [List Form Integrations](actions/list-form-integrations.md) | GET | Lists integrations for an OpnForm form. |
| [Update Webhook Integration](actions/update-webhook-integration.md) | PUT | Updates an existing webhook integration in OpnForm. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Workspace Invite](actions/cancel-workspace-invite.md) | DELETE | Cancels an invite in an OpnForm workspace. |
| [List Workspace Invites](actions/list-workspace-invites.md) | GET | Lists invites in an OpnForm workspace. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Workspace User](actions/add-workspace-user.md) | POST | Adds a user to an OpnForm workspace. |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Lists users in an OpnForm workspace. |
| [Remove Workspace User](actions/remove-workspace-user.md) | DELETE | Removes a user from an OpnForm workspace. |
| [Update Workspace User Role](actions/update-workspace-user-role.md) | PUT | Updates a user's role in an OpnForm workspace. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in OpnForm. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from OpnForm. |
| [List Workspaces](actions/list-workspaces.md) | GET | Lists all workspaces in the OpnForm account. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in OpnForm. |

