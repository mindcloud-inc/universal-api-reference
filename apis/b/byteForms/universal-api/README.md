# <img src="https://images.mindcloud.co/apps/icons/byteformslogo_1775656816537.png" alt="ByteForms logo" width="28" height="28"> ByteForms: Universal API

Create forms, collect responses, manage workspaces, and analyze submissions in ByteForms.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/byteForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forms.bytesuite.io
- **Vendor API docs:** https://forms.bytesuite.io/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Response](actions/delete-response.md) | DELETE |  |
| [Export Responses CSV](actions/export-responses-csv.md) | GET |  |
| [Export Responses XLSX](actions/export-responses-xlsx.md) | GET |  |
| [Get Form Responses](actions/get-form-responses.md) | GET | Retrieves responses for a ByteForms form by form ID. |
| [Get Response](actions/get-response.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Delete Form](actions/delete-form.md) | DELETE |  |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from ByteForms by form ID. |
| [Get Form Analytics](actions/get-form-analytics.md) | GET |  |
| [Get Public Form](actions/get-public-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms created by the current ByteForms user. |
| [Update Form](actions/update-form.md) | PUT |  |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Get Invited Members](actions/get-invited-members.md) | GET |  |
| [List Workspace Invites](actions/list-workspace-invites.md) | GET |  |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Members](actions/get-workspace-members.md) | GET |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Limits](actions/get-subscription-limits.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Subscription](actions/get-active-subscription.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Update Current User](actions/update-current-user.md) | PUT |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

