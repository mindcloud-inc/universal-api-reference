# <img src="https://images.mindcloud.co/apps/icons/deftform-icon_1778175804318.png" alt="Deftform logo" width="28" height="28"> Deftform: Universal API

Build forms, collect responses, manage form fields, generate submission PDFs, and update supported form settings through the Deftform API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deftform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://deftform.com/
- **Vendor API docs:** https://help.deftform.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms and fields from Deftform. |
| [Update Form Settings](actions/update-form-settings.md) | PUT | Updates existing form settings in Deftform. |

### Form Field

| Action | Method | Description |
| --- | --- | --- |
| [List Form Fields](actions/list-form-fields.md) | GET | Retrieves fields for a form from Deftform. |

### Form Response

| Action | Method | Description |
| --- | --- | --- |
| [Add Form Response](actions/add-form-response.md) | POST | Creates a form response in Deftform. |
| [List Form Responses](actions/list-form-responses.md) | GET | Retrieves responses for a form from Deftform. |

### Submission Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Get Submission PDF](actions/get-submission-pdf.md) | GET | Retrieves a submission PDF link from Deftform. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves your workspace details from Deftform. |

