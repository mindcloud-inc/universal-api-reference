# <img src="https://images.mindcloud.co/apps/icons/wufoo_1772822043281.png" alt="Wufoo logo" width="28" height="28"> Wufoo: Universal API

Build forms, collect entries, accept payments, and review reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wufoo/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wufoo.com/
- **Vendor API docs:** https://wufoo.github.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from Wufoo by identifier. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Wufoo. |

### Form Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Form Comments](actions/list-form-comments.md) | GET | Retrieves comments from a specific Wufoo form. |

### Form Comment Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Form Comments](actions/count-form-comments.md) | GET | Retrieves the comment count for a Wufoo form. |

### Form Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Form Entries](actions/list-form-entries.md) | GET | Retrieves entries from a specific Wufoo form. |
| [Submit Form Entry](actions/submit-form-entry.md) | POST | Creates a new entry in a specific Wufoo form. |

### Form Entry Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Form Entries](actions/count-form-entries.md) | GET | Retrieves the entry count for a Wufoo form. |

### Form Field

| Action | Method | Description |
| --- | --- | --- |
| [List Form Fields](actions/list-form-fields.md) | GET | Retrieves fields from a specific Wufoo form. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Wufoo by identifier. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Wufoo. |

### Report Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Report Entries](actions/list-report-entries.md) | GET | Retrieves entries from a specific Wufoo report. |

### Report Entry Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Report Entries](actions/count-report-entries.md) | GET | Retrieves the entry count for a Wufoo report. |

### Report Field

| Action | Method | Description |
| --- | --- | --- |
| [List Report Fields](actions/list-report-fields.md) | GET | Retrieves fields from a specific Wufoo report. |

### Report Widget

| Action | Method | Description |
| --- | --- | --- |
| [List Report Widgets](actions/list-report-widgets.md) | GET | Retrieves widgets from a specific Wufoo report. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Wufoo. |

