# <img src="https://images.mindcloud.co/apps/icons/optform_1775502949140.png" alt="Optform logo" width="28" height="28"> Optform: Universal API

Optform is a form-building and response-management platform for creating forms, managing questions, collecting responses, and administering workspaces, tenants, and contacts through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/optform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://optform.com
- **Vendor API docs:** https://optform.com/help/api/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Form Responses](actions/list-form-responses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optform/latest/actions/list-form-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Optform. |

### Form Question

| Action | Method | Description |
| --- | --- | --- |
| [Add Long Text Question](actions/add-long-text-question.md) | POST | Creates a new long-text question in an Optform form. |
| [Get Form Questions](actions/get-form-questions.md) | GET | Retrieves questions for a specific Optform form. |
| [Remove Question](actions/remove-question.md) | DELETE | Deletes a question from an Optform form. |
| [Update Long Text Question](actions/update-long-text-question.md) | PUT | Updates an existing long-text question in an Optform form. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Form Responses](actions/list-form-responses.md) | GET | Retrieves form responses from Optform. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Optform. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from Optform. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Optform. |
| [List User Forms](actions/list-user-forms.md) | GET | Retrieves forms created by a specific Optform user. |
| [List Workspace Forms](actions/list-workspace-forms.md) | GET | Retrieves forms from a specific Optform workspace. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Optform. |

### Lead Score

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Scores](actions/list-lead-scores.md) | GET | Retrieves lead scores from Optform. |

