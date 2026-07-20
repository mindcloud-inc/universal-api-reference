# <img src="https://images.mindcloud.co/apps/icons/translate-plus_1774972220988.png" alt="TranslatePlus logo" width="28" height="28"> TranslatePlus: Universal API

Translate text, localize files, and monitor translation jobs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/translatePlus/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://translateplus.io
- **Vendor API docs:** https://docs.translateplus.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Summary](actions/get-account-summary.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/get-account-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Batch Translation

| Action | Method | Description |
| --- | --- | --- |
| [Batch Translate Text](actions/batch-translate-text.md) | POST | Translates multiple texts in one TranslatePlus request. |

### Email Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Email](actions/translate-email.md) | POST | Translates email subject and HTML body in TranslatePlus. |

### Html Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate HTML](actions/translate-html.md) | POST | Translates HTML content in TranslatePlus while preserving structure. |

### I18n Job

| Action | Method | Description |
| --- | --- | --- |
| [Create I18n Translation Job](actions/create-i18n-translation-job.md) | POST | Creates a new i18n translation job in TranslatePlus. |
| [Delete I18n Job](actions/delete-i18n-job.md) | DELETE | Deletes an existing i18n translation job from TranslatePlus. |
| [Get I18n Job Status](actions/get-i18n-job-status.md) | GET | Retrieves i18n translation job status from TranslatePlus. |
| [List I18n Jobs](actions/list-i18n-jobs.md) | GET | Retrieves i18n translation jobs from TranslatePlus. |

### Language Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Language](actions/detect-language.md) | POST | Detects the language of provided text in TranslatePlus. |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Summary](actions/get-account-summary.md) | GET | Retrieves account summary and credit usage from TranslatePlus. |

### Service Status

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves API health status from TranslatePlus. |

### Subtitle Translation

| Action | Method | Description |
| --- | --- | --- |
| [Translate Subtitles](actions/translate-subtitles.md) | POST | Translates subtitle files in TranslatePlus while preserving timing. |

### Supported Languages

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Languages](actions/get-supported-languages.md) | GET | Retrieves supported languages and codes from TranslatePlus. |

### Translated File

| Action | Method | Description |
| --- | --- | --- |
| [Download I18n File](actions/download-i18n-file.md) | GET | Downloads a translated i18n file from TranslatePlus. |

### Translation Result

| Action | Method | Description |
| --- | --- | --- |
| [Translate Text](actions/translate-text.md) | POST | Translates text between languages in TranslatePlus. |

