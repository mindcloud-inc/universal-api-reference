# <img src="https://images.mindcloud.co/apps/icons/neeto-form_1774292022019.png" alt="NeetoForm logo" width="28" height="28"> NeetoForm: Universal API

List forms, review submissions, and manage workspace team members

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neetoForm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://neetoform.com
- **Vendor API docs:** https://apidocs.neetoform.com/getting-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from a NeetoForm workspace. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions for a NeetoForm form. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | POST | Adds team members to a NeetoForm workspace. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from a NeetoForm workspace. |
| [Remove Team Members](actions/remove-team-members.md) | DELETE |  |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates an existing team member in NeetoForm. |

