# <img src="https://images.mindcloud.co/apps/icons/simple-localize_1775504684082.png" alt="SimpleLocalize logo" width="28" height="28"> SimpleLocalize: Universal API

Manage translations, languages, keys, and localization workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleLocalize/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://simplelocalize.io
- **Vendor API docs:** https://simplelocalize.io/docs/api/get-started/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Details](actions/get-project-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Project Activity](actions/list-project-activity.md) | GET | Retrieves project activity from SimpleLocalize. |
| [List Project Activity Changes](actions/list-project-activity-changes.md) | GET | Retrieves project activity changes from SimpleLocalize. |

### Auto-translation Job

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Translate Text](actions/auto-translate-text.md) | POST | Creates an auto-translation job for text in SimpleLocalize. |
| [Create Auto-Translation Jobs](actions/create-auto-translation-jobs.md) | POST | Creates auto-translation jobs in SimpleLocalize. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from SimpleLocalize. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from SimpleLocalize. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in SimpleLocalize. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from SimpleLocalize. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from SimpleLocalize. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from SimpleLocalize. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in SimpleLocalize. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | POST | Creates a new environment in SimpleLocalize. |
| [Get Environment Status](actions/get-environment-status.md) | GET | Retrieves environment status from SimpleLocalize. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from SimpleLocalize. |
| [Publish Translations](actions/publish-translations.md) | PUT | Publishes translations to an environment in SimpleLocalize. |

### Export Job

| Action | Method | Description |
| --- | --- | --- |
| [Export Translations](actions/export-translations.md) | GET | Exports translations from SimpleLocalize as files. |

### Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Import Translations](actions/import-translations.md) | POST | Imports translations from a file into SimpleLocalize. |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [Create Language](actions/create-language.md) | POST | Creates a new language in SimpleLocalize. |
| [Delete Language](actions/delete-language.md) | DELETE | Deletes an existing language from SimpleLocalize. |
| [Get Language](actions/get-language.md) | GET | Retrieves a language from SimpleLocalize. |
| [List Languages](actions/list-languages.md) | GET | Retrieves languages from SimpleLocalize. |
| [Update Language](actions/update-language.md) | PUT | Updates an existing language in SimpleLocalize. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from SimpleLocalize. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in SimpleLocalize. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from SimpleLocalize. |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves project tags from SimpleLocalize. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in SimpleLocalize. |

### Translation

| Action | Method | Description |
| --- | --- | --- |
| [List Translations](actions/list-translations.md) | GET | Retrieves translations from SimpleLocalize. |
| [Update Translation](actions/update-translation.md) | PUT | Updates a single translation in SimpleLocalize. |
| [Update Translations in Bulk](actions/update-translations-in-bulk.md) | PUT | Updates translations in bulk in SimpleLocalize. |

### Translation Key

| Action | Method | Description |
| --- | --- | --- |
| [Create Translation Key](actions/create-translation-key.md) | POST | Creates a new translation key in SimpleLocalize. |
| [Create Translation Keys in Bulk](actions/create-translation-keys-in-bulk.md) | POST | Creates translation keys in bulk in SimpleLocalize. |
| [Delete Translation Key](actions/delete-translation-key.md) | DELETE | Deletes a translation key from SimpleLocalize. |
| [Get Translation Key Details](actions/get-translation-key-details.md) | GET | Retrieves translation key details from SimpleLocalize. |
| [List Translation Keys](actions/list-translation-keys.md) | GET | Retrieves translation keys from SimpleLocalize without metadata. |
| [List Translation Keys V2](actions/list-translation-keys-v2.md) | GET | Retrieves translation keys from SimpleLocalize without metadata. |
| [List Translation Keys With Metadata](actions/list-translation-keys-with-metadata.md) | GET | Retrieves translation keys with metadata from SimpleLocalize. |
| [Update Translation Key](actions/update-translation-key.md) | PUT | Updates an existing translation key in SimpleLocalize. |
| [Update Translation Key by ID](actions/update-translation-key-by-id.md) | PUT | Updates an existing translation key by ID in SimpleLocalize. |

