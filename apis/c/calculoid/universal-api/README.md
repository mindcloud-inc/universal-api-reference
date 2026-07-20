# <img src="https://images.mindcloud.co/apps/icons/calculoid_1776880347359.png" alt="Calculoid logo" width="28" height="28"> Calculoid: Universal API

Calculoid is a web calculator builder for creating, publishing, analyzing, and integrating interactive calculators.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/calculoid/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.calculoid.com/
- **Vendor API docs:** https://www.calculoid.com/documentation-new

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Calculator](actions/get-calculator.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/get-calculator?connectionId=$CONNECTION_ID&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST |  |
| [Delete Table](actions/delete-table.md) | DELETE |  |
| [Get Table](actions/get-table.md) | GET |  |
| [List Tables](actions/list-tables.md) | GET |  |
| [Update Table](actions/update-table.md) | PUT |  |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Submission](actions/delete-submission.md) | DELETE |  |
| [Get Result](actions/get-result.md) | GET |  |
| [Get Submission](actions/get-submission.md) | GET |  |
| [List Calculator Results](actions/list-calculator-results.md) | GET |  |
| [List Submissions](actions/list-submissions.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Copy Calculator](actions/copy-calculator.md) | POST |  |
| [Delete Calculator](actions/delete-calculator.md) | DELETE |  |
| [Get Calculator](actions/get-calculator.md) | GET |  |
| [Import Calculator](actions/import-calculator.md) | POST |  |
| [List Calculators](actions/list-calculators.md) | GET |  |
| [Rate Calculator](actions/rate-calculator.md) | PUT |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Geo IP](actions/get-geo-ip.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Calculator Report](actions/get-calculator-report.md) | GET |  |
| [List Statistic Domains](actions/list-statistic-domains.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Calculator Templates](actions/list-calculator-templates.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Field Option](actions/create-field-option.md) | POST |  |
| [Delete Field](actions/delete-field.md) | DELETE |  |
| [Delete Field Option](actions/delete-field-option.md) | DELETE |  |
| [List Languages](actions/list-languages.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [List Calculator Webhooks](actions/list-calculator-webhooks.md) | GET |  |

