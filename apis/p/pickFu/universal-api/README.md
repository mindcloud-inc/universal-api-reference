# <img src="https://images.mindcloud.co/apps/icons/pickfu-icon-filled-256_1774973670513.png" alt="PickFu logo" width="28" height="28"> PickFu: Universal API

Build and manage PickFu surveys, audience targeting traits, projects, tags, playbooks, and survey responses from MindCloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pickFu/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pickfu.com
- **Vendor API docs:** https://www.pickfu.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Surveys](actions/list-surveys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Audiences

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting Traits](actions/get-reporting-traits.md) | GET |  |
| [Get Targeting Traits](actions/get-targeting-traits.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Survey](actions/create-survey.md) | POST |  |
| [Delete Survey](actions/delete-survey.md) | DELETE |  |
| [Get Survey](actions/get-survey.md) | GET |  |
| [Get Survey Responses](actions/get-survey-responses.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |
| [Update Survey](actions/update-survey.md) | PUT |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Playbooks](actions/list-playbooks.md) | GET |  |
| [Search Help Articles](actions/search-help-articles.md) | GET |  |

