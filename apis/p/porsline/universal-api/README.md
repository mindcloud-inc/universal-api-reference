# <img src="https://images.mindcloud.co/apps/icons/porsline_1774885936800.png" alt="Porsline logo" width="28" height="28"> Porsline: Universal API

Create surveys and forms, collect responses, and analyze results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/porsline/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://porsline.com/en
- **Vendor API docs:** https://developers.porsline.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Authentication Code

| Action | Method | Description |
| --- | --- | --- |
| [Create Authentication Codes](actions/create-authentication-codes.md) | POST |  |
| [Delete Authentication Codes](actions/delete-authentication-codes.md) | DELETE |  |
| [List Survey Authentication Codes](actions/list-survey-authentication-codes.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Replace Folder](actions/replace-folder.md) | PUT |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Hidden Field Hash

| Action | Method | Description |
| --- | --- | --- |
| [Hash Hidden Fields](actions/hash-hidden-fields.md) | POST |  |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Create Notification](actions/create-notification.md) | POST |  |
| [Get Notification](actions/get-notification.md) | GET |  |
| [List Notifications](actions/list-notifications.md) | GET |  |
| [Update Notification](actions/update-notification.md) | PUT |  |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST |  |
| [Delete Question](actions/delete-question.md) | DELETE |  |
| [Get Question](actions/get-question.md) | GET |  |
| [Update Question](actions/update-question.md) | PUT |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Delete Survey](actions/delete-survey.md) | DELETE |  |
| [Retrieve Survey](actions/retrieve-survey.md) | GET |  |

### Survey Response Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Responses Export](actions/get-survey-responses-export.md) | GET |  |

### Survey Response Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Responses Results Table](actions/get-survey-responses-results-table.md) | GET |  |

### Survey Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Settings](actions/get-survey-settings.md) | GET |  |
| [Update Survey Settings](actions/update-survey-settings.md) | PUT |  |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Variables](actions/create-variables.md) | POST |  |
| [List Survey Variables](actions/list-survey-variables.md) | GET |  |

