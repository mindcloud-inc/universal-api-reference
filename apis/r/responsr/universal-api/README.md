# <img src="https://images.mindcloud.co/apps/icons/cropped-favicon-450x450-2_1775063510605.png" alt="Responsr logo" width="28" height="28"> Responsr: Universal API

Responsr is a customer and employee feedback platform for surveys, projects, respondents, analytics, and operational follow-up.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/responsr/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://responsr.io
- **Vendor API docs:** https://app.responsr.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | GET |  |
| [Get Default Access Token](actions/get-default-access-token.md) | GET |  |
| [List Access Tokens](actions/list-access-tokens.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Person](actions/get-default-person.md) | GET |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List Persons](actions/list-persons.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Project Variable](actions/get-default-project-variable.md) | GET |  |
| [Get Project Variable](actions/get-project-variable.md) | GET |  |
| [List Project Variables](actions/list-project-variables.md) | GET |  |
| [List Variables](actions/list-variables.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Project Survey](actions/get-default-project-survey.md) | GET |  |
| [Get Project Survey](actions/get-project-survey.md) | GET |  |
| [List Project Surveys](actions/list-project-surveys.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Default User Group](actions/get-default-user-group.md) | GET |  |
| [Get User Group](actions/get-user-group.md) | GET |  |
| [List User Groups](actions/list-user-groups.md) | GET |  |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Case](actions/get-project-case.md) | GET |  |
| [List Project Cases](actions/list-project-cases.md) | GET |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Notification](actions/get-project-notification.md) | GET |  |
| [List Notifications](actions/list-notifications.md) | GET |  |
| [List Project Notifications](actions/list-project-notifications.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Project](actions/get-default-project.md) | GET |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Dashboard](actions/get-project-dashboard.md) | GET |  |
| [Get Project Result](actions/get-project-result.md) | GET |  |
| [List Project Dashboards](actions/list-project-dashboards.md) | GET |  |
| [List Project Results](actions/list-project-results.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Language](actions/get-default-language.md) | GET |  |
| [Get Language](actions/get-language.md) | GET |  |
| [List Languages](actions/list-languages.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Default User](actions/get-default-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Project Users](actions/list-project-users.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Project Webhook](actions/get-default-project-webhook.md) | GET |  |
| [Get Project Webhook](actions/get-project-webhook.md) | GET |  |
| [List Project Webhooks](actions/list-project-webhooks.md) | GET |  |

### Webhook Events

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET |  |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Task](actions/get-async-task.md) | GET |  |
| [List Async Tasks](actions/list-async-tasks.md) | GET |  |

