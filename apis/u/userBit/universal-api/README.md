# <img src="https://images.mindcloud.co/apps/icons/user-bit_1775235156546.png" alt="UserBit logo" width="28" height="28"> UserBit: Universal API

Research customer feedback, manage repository notes, browse projects, and work with surveys in UserBit.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/userBit/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://userbit.com/
- **Vendor API docs:** https://userbit.com/content/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Note](actions/create-or-update-note.md) | PUT | Creates or updates a note in UserBit. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves repository projects from a UserBit workspace. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey Response](actions/create-survey-response.md) | POST | Creates a survey response in UserBit. |
| [List Insights](actions/list-insights.md) | GET | Retrieves insights from a UserBit repository project. |
| [List Survey Questions](actions/list-survey-questions.md) | GET | Retrieves survey questions from a UserBit survey. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from a UserBit repository project. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves accessible workspaces from the UserBit account. |

