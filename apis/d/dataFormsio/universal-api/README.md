# <img src="https://images.mindcloud.co/apps/icons/dataforms-icon-square_1775487104777.png" alt="DataForms.io logo" width="28" height="28"> DataForms.io: Universal API

Access DataForms.io templates, fields, forms, entries, and current-user data through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataFormsio/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dataforms.io
- **Vendor API docs:** https://dataforms.readme.io/reference/getting-started-with-your-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Form](actions/create-data-form.md) | POST | Creates a new data form in DataForms.io. |
| [Delete Data Form](actions/delete-data-form.md) | DELETE | Deletes an existing data form from DataForms.io. |
| [Get Data Form](actions/get-data-form.md) | GET | Retrieves a data form from DataForms.io. |
| [List Data Forms](actions/list-data-forms.md) | GET | Retrieves data forms from DataForms.io. |
| [Update Data Form](actions/update-data-form.md) | PUT | Updates an existing data form in DataForms.io. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from DataForms.io. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from DataForms.io. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in DataForms.io. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Entry](actions/get-entry.md) | GET | Retrieves an entry from DataForms.io. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from DataForms.io. |
| [List Entries](actions/list-entries.md) | GET | Retrieves entries from DataForms.io. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from DataForms.io. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from DataForms.io. |

