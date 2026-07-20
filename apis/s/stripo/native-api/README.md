# Stripo: Native API Reference

A consolidated summary of Stripo's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://api.stripo.email/
- **API base URL:** `https://my.stripo.email/emailgeneration/v1`

## Authentication

### Project API Key

Stripo project REST API JWT generated from project settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Stripo-Api-Auth: <apiKey>
```

[Official authentication documentation](https://api.stripo.email/docs/authentication)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Email Translations JSON](actions/apply-email-translations-json.md) | `POST /emails/:id/translation-versions/json/apply` | [docs](https://api.stripo.email/reference/applyemailtranslationjson) |
| [Apply Template Translations JSON](actions/apply-template-translations-json.md) | `POST /templates/:id/translation-versions/json/apply` | [docs](https://api.stripo.email/reference/applytemplatetranslationjson) |
| [Create Email Translation Versions](actions/create-email-translation-versions.md) | `POST /emails/:id/translation-versions` | [docs](https://api.stripo.email/reference/createemailtranslationversions) |
| [Create SRT Transformer](actions/create-srt-transformer.md) | `POST /srt` | [docs](https://api.stripo.email/reference/savesrtconfig) |
| [Create Template Translation Versions](actions/create-template-translation-versions.md) | `POST /templates/:id/translation-versions` | [docs](https://api.stripo.email/reference/createtemplatetranslationversions) |
| [Delete Email](actions/delete-email.md) | `DELETE /emails/:id` | [docs](https://api.stripo.email/reference/deleteemail) |
| [Delete SRT Transformer](actions/delete-srt-transformer.md) | `DELETE /srt` | [docs](https://api.stripo.email/reference/deletesrtconfig) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:id` | [docs](https://api.stripo.email/reference/deletetemplate) |
| [Download Email Translations JSON](actions/download-email-translations-json.md) | `POST /emails/:id/translation-versions/json` | [docs](https://api.stripo.email/reference/createemailtranslationjson) |
| [Download Template Translations JSON](actions/download-template-translations-json.md) | `POST /templates/:id/translation-versions/json` | [docs](https://api.stripo.email/reference/createtemplatetranslationjson) |
| [Export Email as HTML](actions/export-email-as-html.md) | `GET /export/html/emails/:id` | [docs](https://api.stripo.email/reference/exportemailtohtmlfile) |
| [Export Email to eSputnik](actions/export-email-to-esputnik.md) | `POST /export/esputnik` | [docs](https://api.stripo.email/reference/exportesputnik) |
| [Export Template as HTML](actions/export-template-as-html.md) | `GET /export/html/templates/:id` | [docs](https://api.stripo.email/reference/exporttemplatetohtmlfile) |
| [Generate Email](actions/generate-email.md) | `POST /email` | [docs](https://api.stripo.email/reference/generateemail) |
| [Get Email](actions/get-email.md) | `GET /emails/:id` | [docs](https://api.stripo.email/reference/getemailbyid) |
| [Get Organization Limits](actions/get-organization-limits.md) | `GET /organizationLimits` | [docs](https://api.stripo.email/reference/getorganizationlimits) |
| [Get Raw Email](actions/get-raw-email.md) | `GET /raw-email/:id` | [docs](https://api.stripo.email/reference/getrawemail) |
| [Get Raw Template](actions/get-raw-template.md) | `GET /raw-template/:id` | [docs](https://api.stripo.email/reference/getrawtemplate) |
| [Get SRT Transformer](actions/get-srt-transformer.md) | `GET /srt` | [docs](https://api.stripo.email/reference/getsrtconfig) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://api.stripo.email/reference/gettemplatebyid) |
| [List Emails](actions/list-emails.md) | `GET /emails` | [docs](https://api.stripo.email/reference/findemails) |
| [List Folders](actions/list-folders.md) | `GET /folders/:type` | [docs](https://api.stripo.email/reference/getfolders) |
| [List Modules](actions/list-modules.md) | `GET /modules` | [docs](https://api.stripo.email/reference/findmodules) |
| [List SRT Transformers](actions/list-srt-transformers.md) | `GET /srtnames` | [docs](https://api.stripo.email/reference/getsrtconfignames) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://api.stripo.email/reference/findtemplates) |
| [Validate Token](actions/validate-token.md) | `GET /validate` | [docs](https://api.stripo.email/reference/validateapitoken) |
