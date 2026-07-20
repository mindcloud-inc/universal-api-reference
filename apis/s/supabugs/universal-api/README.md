# <img src="https://images.mindcloud.co/apps/icons/supabugs-favicon-go_1775592227441.png" alt="Supabugs logo" width="28" height="28"> Supabugs: Universal API

API-first issue tracker for reporting, tracking, and resolving bugs across client and internal projects.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/supabugs/latest
- **Category:** Productivity / Project Management
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.supabugs.io/
- **Vendor API docs:** https://api.supabugs.io/api/public/v1/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project](actions/get-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Supabugs. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Supabugs. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Supabugs by ID. |
| [List Issues](actions/list-issues.md) | GET | Retrieves the latest 20 issues from Supabugs. |
| [Search Issues](actions/search-issues.md) | GET | Finds issues in Supabugs by search criteria. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Supabugs. |

### Issueattachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Issue Attachment](actions/delete-issue-attachment.md) | DELETE | Deletes an attachment from a Supabugs issue. |
| [Upload Issue Attachment](actions/upload-issue-attachment.md) | POST | Uploads a new attachment to a Supabugs issue. |

### Issuecomment

| Action | Method | Description |
| --- | --- | --- |
| [Add Issue Comment](actions/add-issue-comment.md) | POST | Creates a new comment on a Supabugs issue. |
| [Delete Issue Comment](actions/delete-issue-comment.md) | DELETE | Deletes a comment from a Supabugs issue. |

### Lookupvalue

| Action | Method | Description |
| --- | --- | --- |
| [List Lookup Values](actions/list-lookup-values.md) | GET | Retrieves issue lookup values from Supabugs. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves current project details from Supabugs. |

