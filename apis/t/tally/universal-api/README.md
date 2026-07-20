# <img src="https://images.mindcloud.co/apps/icons/tally-square-background-removed-1_1763397891885.png" alt="Tally logo" width="28" height="28"> Tally: Universal API

Build forms, collect payments, capture submissions, and automate follow-ups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tally/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tally.so/
- **Vendor API docs:** https://developers.tally.so/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form](actions/delete-form.md) | DELETE |  |
| [Get Form](actions/get-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |

### Form Question

| Action | Method | Description |
| --- | --- | --- |
| [List Form Questions](actions/list-form-questions.md) | GET |  |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form Submission](actions/delete-form-submission.md) | DELETE |  |
| [Get Form Submission](actions/get-form-submission.md) | GET |  |
| [List Form Submissions](actions/list-form-submissions.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invite](actions/cancel-invite.md) | DELETE |  |
| [Create Invite](actions/create-invite.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User Info](actions/get-user-info.md) | GET |  |
| [List Invites](actions/list-invites.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | GET |  |

