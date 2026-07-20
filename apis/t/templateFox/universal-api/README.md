# <img src="https://images.mindcloud.co/apps/icons/template-fox_1775667898163.png" alt="TemplateFox logo" width="28" height="28"> TemplateFox: Universal API

Generate PDFs from templates, inspect account credits, and manage TemplateFox templates through the API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/templateFox/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://templatefox.com
- **Vendor API docs:** https://templatefox.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templateFox/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from TemplateFox. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | POST | Creates a PDF from a template in TemplateFox. |

### Pdf Job

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF Async](actions/create-pdf-async.md) | POST | Creates a PDF generation job in TemplateFox. |
| [Get PDF Job](actions/get-pdf-job.md) | GET | Retrieves a PDF job from TemplateFox. |
| [List PDF Jobs](actions/list-pdf-jobs.md) | GET | Retrieves PDF jobs from TemplateFox. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from TemplateFox. |

### Template Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Fields](actions/get-template-fields.md) | GET | Retrieves template fields from TemplateFox. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves account transactions from TemplateFox. |

