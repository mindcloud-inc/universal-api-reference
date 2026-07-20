# <img src="https://images.mindcloud.co/apps/icons/formstack_1773180056232.png" alt="Formstack logo" width="28" height="28"> Formstack: Universal API

Build forms, collect submissions, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formstack/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.formstack.com
- **Vendor API docs:** https://developers.formstack.com/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Field](actions/create-form-field.md) | POST | Creates a new field in a Formstack form. |
| [Delete Form Field](actions/delete-form-field.md) | DELETE | Permanently deletes a field from a Formstack form. |
| [Get Form Field](actions/get-form-field.md) | GET | Retrieves a field from a Formstack form. |
| [List Form Fields](actions/list-form-fields.md) | GET | Retrieves fields for a form from Formstack. |
| [Update Form Field](actions/update-form-field.md) | PUT | Updates an existing field in a Formstack form. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Formstack. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves details for a folder from Formstack. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders and subfolders from Formstack. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Copy Form](actions/copy-form.md) | POST | Creates a copy of a form in Formstack. |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Formstack. |
| [Create Form Prefill URL](actions/create-form-prefill-url.md) | POST | Generates a prefilled form URL in Formstack. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes a form from Formstack by marking it as deleted. |
| [Get Form](actions/get-form.md) | GET | Retrieves details for a form from Formstack. |
| [Get Form HTML](actions/get-form-html.md) | GET | Retrieves HTML markup for a form from Formstack. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Formstack with filtering and sorting. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Formstack. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Submission](actions/create-submission.md) | POST | Creates a new submission in Formstack. |
| [Delete Submission](actions/delete-submission.md) | DELETE | Permanently deletes a submission and its associated data from Formstack. |
| [Get Submission](actions/get-submission.md) | GET | Retrieves details for a submission from Formstack. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves submissions for a form from Formstack. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions across all forms from Formstack. |
| [Update Submission](actions/update-submission.md) | PUT | Updates an existing submission in Formstack. |

### Submission Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Form Submissions](actions/count-form-submissions.md) | GET | Retrieves submission counts for a form from Formstack. |

### Submission Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Submission Upload](actions/get-submission-upload.md) | GET | Retrieves an uploaded file from a Formstack submission. |

