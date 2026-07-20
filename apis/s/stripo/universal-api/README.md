# <img src="https://images.mindcloud.co/apps/icons/images-24_1776776047196.png" alt="Stripo logo" width="28" height="28"> Stripo: Universal API

Stripo is an email template builder API for generating, managing, translating, and exporting responsive email templates and messages from a Stripo project.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stripo/latest
- **Category:** Communication / Email Communications
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stripo.email/
- **Vendor API docs:** https://api.stripo.email/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Token](actions/validate-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Validate Token](actions/validate-token.md) | GET | Validates a Stripo API token. |

### Email Templates

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Stripo. |
| [Get Raw Template](actions/get-raw-template.md) | GET | Retrieves raw HTML and CSS for a template from Stripo. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Stripo. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Stripo. |

### Email Translation Version

| Action | Method | Description |
| --- | --- | --- |
| [Apply Email Translations JSON](actions/apply-email-translations-json.md) | PUT | Applies email translations from a JSON file in Stripo. |
| [Create Email Translation Versions](actions/create-email-translation-versions.md) | POST | Creates translation versions for an email in Stripo. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an email from Stripo. |
| [Export Email to eSputnik](actions/export-email-to-esputnik.md) | POST | Exports an email from Stripo to eSputnik. |
| [Generate Email](actions/generate-email.md) | POST | Generates an email in Stripo from external source data. |
| [Get Email](actions/get-email.md) | GET | Retrieves an email from Stripo. |
| [Get Raw Email](actions/get-raw-email.md) | GET | Retrieves raw HTML and CSS for an email from Stripo. |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails from Stripo. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Email Translations JSON](actions/download-email-translations-json.md) | GET | Downloads email translations as a JSON file from Stripo. |
| [Download Template Translations JSON](actions/download-template-translations-json.md) | GET | Downloads template translations as a JSON file from Stripo. |
| [Export Email as HTML](actions/export-email-as-html.md) | GET | Exports an email as an HTML file from Stripo. |
| [Export Template as HTML](actions/export-template-as-html.md) | GET | Exports a template as an HTML file from Stripo. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Stripo by type. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [List Modules](actions/list-modules.md) | GET | Retrieves saved modules from Stripo. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Limits](actions/get-organization-limits.md) | GET | Retrieves organization limits from Stripo. |

### Srt Transformer

| Action | Method | Description |
| --- | --- | --- |
| [Create SRT Transformer](actions/create-srt-transformer.md) | POST | Creates an SRT transformer in Stripo. |
| [Delete SRT Transformer](actions/delete-srt-transformer.md) | DELETE | Deletes an SRT transformer from Stripo. |
| [Get SRT Transformer](actions/get-srt-transformer.md) | GET | Retrieves an SRT transformer configuration from Stripo. |
| [List SRT Transformers](actions/list-srt-transformers.md) | GET | Retrieves SRT transformers from Stripo. |

### Template Translation Version

| Action | Method | Description |
| --- | --- | --- |
| [Apply Template Translations JSON](actions/apply-template-translations-json.md) | PUT | Applies template translations from a JSON file in Stripo. |
| [Create Template Translation Versions](actions/create-template-translation-versions.md) | POST | Creates translation versions for a template in Stripo. |

