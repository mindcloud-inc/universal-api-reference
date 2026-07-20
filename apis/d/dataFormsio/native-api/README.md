# DataForms.io: Native API Reference

A consolidated summary of DataForms.io's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://dataforms.readme.io/reference/getting-started-with-your-api
- **API base URL:** `https://api.dataforms.io`

## Authentication

### API Key

Use a DataForms.io API key from Settings > Security.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dataforms.readme.io/reference/getting-started-with-your-api)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Data Form](actions/create-data-form.md) | `POST /dataforms` | [docs](https://dataforms.readme.io/reference/update-data-form-copy) |
| [Delete Data Form](actions/delete-data-form.md) | `DELETE /dataforms/{form_id}` | [docs](https://dataforms.readme.io/reference/store-data-form-copy) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://dataforms.readme.io/reference/show-user) |
| [Get Data Form](actions/get-data-form.md) | `GET /dataforms/{form_id}` | [docs](https://dataforms.readme.io/reference/index-data-forms-copy) |
| [Get Entry](actions/get-entry.md) | `GET /entries/{entry_id}` | [docs](https://dataforms.readme.io/reference/index-entries-copy) |
| [Get Field](actions/get-field.md) | `GET /templates/{template_id}/fields/{field_id}` | [docs](https://dataforms.readme.io/reference/index-fields-copy) |
| [Get Template](actions/get-template.md) | `GET /templates/{template_id}` | [docs](https://dataforms.readme.io/reference/index-templates-copy) |
| [List Data Forms](actions/list-data-forms.md) | `GET /dataforms` | [docs](https://dataforms.readme.io/reference/index-data-forms) |
| [List Entries](actions/list-entries.md) | `GET /entries` | [docs](https://dataforms.readme.io/reference/index-entries) |
| [List Fields](actions/list-fields.md) | `GET /templates/{template_id}/fields` | [docs](https://dataforms.readme.io/reference/index-fields) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://dataforms.readme.io/reference/index-templates) |
| [Update Data Form](actions/update-data-form.md) | `PUT /dataforms/{form_id}` | [docs](https://dataforms.readme.io/reference/show-data-form-copy) |
| [Update Template](actions/update-template.md) | `PUT /templates/{template_id}` | [docs](https://dataforms.readme.io/reference/show-template-copy) |
