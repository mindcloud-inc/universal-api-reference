# <img src="https://images.mindcloud.co/apps/icons/satismeter_1773787509905.png" alt="SatisMeter logo" width="28" height="28"> SatisMeter: Universal API

Manage surveys, responses, users, and feedback analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/satisMeter/latest
- **Category:** Support / Customer Success
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://satismeter.com
- **Vendor API docs:** https://app.satismeter.com/apidoc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project](actions/get-project.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey](actions/get-survey.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Statistics](actions/get-survey-statistics.md) | GET |  |

### Satisfaction Responses

| Action | Method | Description |
| --- | --- | --- |
| [Insert NPS Survey Response](actions/insert-nps-survey-response.md) | POST |  |
| [List Project Responses](actions/list-project-responses.md) | GET |  |
| [List Survey Responses](actions/list-survey-responses.md) | GET |  |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [List Unsubscribed Emails](actions/list-unsubscribed-emails.md) | GET |  |
| [Update Unsubscribed Emails](actions/update-unsubscribed-emails.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [List Users](actions/list-users.md) | GET |  |
| [Upsert User](actions/upsert-user.md) | PUT |  |

