# <img src="https://images.mindcloud.co/apps/icons/favicon-intercom-help-48x48_1776087364279.png" alt="PromptHub logo" width="28" height="28"> PromptHub: Universal API

Manage PromptHub projects, retrieve prompts, and run prompt revisions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/promptHub/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.prompthub.us
- **Vendor API docs:** https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptHub/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects for a PromptHub team. |

### Project Head

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Head](actions/get-project-head.md) | GET | Retrieves a PromptHub project's head revision. |

### Project Run

| Action | Method | Description |
| --- | --- | --- |
| [Run Project](actions/run-project.md) | POST | Runs a PromptHub project by project ID. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from PromptHub. |

