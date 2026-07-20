# SimpleLocalize: Native API Reference

A consolidated summary of SimpleLocalize's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://simplelocalize.io/docs/api/get-started/
- **OpenAPI specification:** https://api.simplelocalize.io/openapi/ui
- **API base URL:** `https://api.simplelocalize.io`

## Authentication

### Project API Key

Connect with a SimpleLocalize project API key from Settings > Credentials > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://simplelocalize.io/docs/api/get-started/)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `size` in the query string to set the page size (default 100; accepted range 0–2500). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auto-Translate Text](actions/auto-translate-text.md) | `POST /api/v1/auto-translate` | [docs](https://api.simplelocalize.io/openapi/ui#/Auto-translation/autoTranslateText) |
| [Create Auto-Translation Jobs](actions/create-auto-translation-jobs.md) | `POST /api/v2/jobs/auto-translate` | [docs](https://api.simplelocalize.io/openapi/ui#/Auto-translation/autoTranslate) |
| [Create Customer](actions/create-customer.md) | `POST /api/v1/customers` | [docs](https://api.simplelocalize.io/openapi/ui#/Customers/createCustomer) |
| [Create Environment](actions/create-environment.md) | `POST /api/v2/environments` | [docs](https://api.simplelocalize.io/openapi/ui#/Hosting/createEnvironment) |
| [Create Language](actions/create-language.md) | `POST /api/v1/languages` | [docs](https://api.simplelocalize.io/openapi/ui#/Languages/createLanguage) |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/tags` | [docs](https://api.simplelocalize.io/openapi/ui#/Tags/createTag) |
| [Create Translation Key](actions/create-translation-key.md) | `POST /api/v1/translation-keys` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/createTranslationKey) |
| [Create Translation Keys in Bulk](actions/create-translation-keys-in-bulk.md) | `POST /api/v1/translation-keys/bulk` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/createTranslationKeyBulk) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /api/v1/customers/{customerKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Customers/deleteCustomer) |
| [Delete Language](actions/delete-language.md) | `DELETE /api/v1/languages/{languageKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Languages/deleteLanguage) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v1/tags/{tagName}` | [docs](https://api.simplelocalize.io/openapi/ui#/Tags/deleteTag) |
| [Delete Translation Key](actions/delete-translation-key.md) | `DELETE /api/v1/translation-keys` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/deleteTranslationKey) |
| [Export Translations](actions/export-translations.md) | `GET /api/v4/export` | [docs](https://api.simplelocalize.io/openapi/ui#/File%20import%20%26%20export/exportTranslations) |
| [Get Customer](actions/get-customer.md) | `GET /api/v1/customers/{customerKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Customers/getCustomer) |
| [Get Environment Status](actions/get-environment-status.md) | `GET /api/v2/environments/{environmentKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Hosting/getEnvironmentStatus) |
| [Get Job](actions/get-job.md) | `GET /api/v2/jobs/{jobId}` | [docs](https://api.simplelocalize.io/openapi/ui#/Auto-translation/getJob) |
| [Get Language](actions/get-language.md) | `GET /api/v1/languages/{languageKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Languages/getLanguage) |
| [Get Project Details](actions/get-project-details.md) | `GET /api/v2/project` | [docs](https://api.simplelocalize.io/openapi/ui#/Projects/getProjectDetailsV2) |
| [Get Translation Key Details](actions/get-translation-key-details.md) | `GET /api/v1/translation-keys/details` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/getTranslationKeyDetails) |
| [Import Translations](actions/import-translations.md) | `POST /api/v2/import` | [docs](https://api.simplelocalize.io/openapi/ui#/File%20import%20%26%20export/importTranslations) |
| [List Customers](actions/list-customers.md) | `GET /api/v1/customers` | [docs](https://api.simplelocalize.io/openapi/ui#/Customers/getAllCustomers) |
| [List Environments](actions/list-environments.md) | `GET /api/v2/environments` | [docs](https://api.simplelocalize.io/openapi/ui#/Hosting/getEnvironments) |
| [List Jobs](actions/list-jobs.md) | `GET /api/v2/jobs` | [docs](https://api.simplelocalize.io/openapi/ui#/Auto-translation/getJobs) |
| [List Languages](actions/list-languages.md) | `GET /api/v1/languages` | [docs](https://api.simplelocalize.io/openapi/ui#/Languages/getLanguages) |
| [List Project Activity](actions/list-project-activity.md) | `GET /api/v1/activity` | [docs](https://api.simplelocalize.io/openapi/ui#/Activity/getActivity) |
| [List Project Activity Changes](actions/list-project-activity-changes.md) | `GET /api/v1/activity/{activityId}/changes` | [docs](https://api.simplelocalize.io/openapi/ui#/Activity/getActivityChanges) |
| [List Project Tags](actions/list-project-tags.md) | `GET /api/v1/tags` | [docs](https://api.simplelocalize.io/openapi/ui#/Tags/getTags) |
| [List Translation Keys](actions/list-translation-keys.md) | `GET /api/v1/translation-keys/list` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/getAllTranslationKeys) |
| [List Translation Keys V2](actions/list-translation-keys-v2.md) | `GET /api/v2/translation-keys/list` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/getAllTranslationKeysV2) |
| [List Translation Keys With Metadata](actions/list-translation-keys-with-metadata.md) | `GET /api/v1/translation-keys` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/getTranslationKeys) |
| [List Translations](actions/list-translations.md) | `GET /api/v2/translations` | [docs](https://api.simplelocalize.io/openapi/ui#/Translations/getTranslations) |
| [Publish Translations](actions/publish-translations.md) | `POST /api/v2/environments/{environmentKey}/publish` | [docs](https://api.simplelocalize.io/openapi/ui#/Hosting/publishTranslations) |
| [Update Customer](actions/update-customer.md) | `PATCH /api/v1/customers/{customerKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Customers/updateCustomer) |
| [Update Language](actions/update-language.md) | `PATCH /api/v1/languages/{languageKey}` | [docs](https://api.simplelocalize.io/openapi/ui#/Languages/updateLanguage) |
| [Update Tag](actions/update-tag.md) | `PATCH /api/v1/tags/{tagName}` | [docs](https://api.simplelocalize.io/openapi/ui#/Tags/updateTag) |
| [Update Translation](actions/update-translation.md) | `PATCH /api/v2/translations` | [docs](https://api.simplelocalize.io/openapi/ui#/Translations/updateTranslations) |
| [Update Translation Key](actions/update-translation-key.md) | `PATCH /api/v1/translation-keys` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/updateTranslationKey) |
| [Update Translation Key by ID](actions/update-translation-key-by-id.md) | `PATCH /api/v1/translation-keys/{id}` | [docs](https://api.simplelocalize.io/openapi/ui#/Translation%20keys/updateTranslationKeyById) |
| [Update Translations in Bulk](actions/update-translations-in-bulk.md) | `PATCH /api/v2/translations/bulk` | [docs](https://api.simplelocalize.io/openapi/ui#/Translations/updateTranslationsBulk) |
