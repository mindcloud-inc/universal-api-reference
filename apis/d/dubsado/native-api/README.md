# Dubsado: Native API Reference

A consolidated summary of Dubsado's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://help.dubsado.com/en/articles/909872-connecting-with-zapier
- **API base URL:** `https://app.dubsado.com/api`

## Authentication

### Session + API Key

Connect Dubsado with a Zapier API key for /zapier/key validation plus live browser request-header values for session-backed web-app actions. Session-backed actions use Cookie, XCSRF Token, and XBrand from the Request Headers section of a logged-in app.dubsado.com API request.

### Credentials

- **API Key:** `apiKey` · required · Zapier API key generated from Dubsado Integrations.
- **Cookie:** `cookie` · optional · Full Cookie value copied from the Request Headers section of an authenticated app.dubsado.com API request.
- **XCSRF Token:** `csrfToken` · optional · x-csrf-token value copied from the Request Headers section of the same authenticated app.dubsado.com API request.
- **XBrand:** `brandId` · optional · x-brand value copied from the Request Headers section of the same authenticated app.dubsado.com API request.

Send these headers with each API request:

```http
Authorization: <apiKey>
Cookie: <cookie>
x-brand: <brandId>
x-csrf-token: <csrfToken>
```

[Official authentication documentation](https://help.dubsado.com/en/articles/909872-connecting-with-zapier)

## API conventions

The total page count is read from `meta.totalPages`. The current page number is read from `meta.currentPage`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Calendar Appointments (Session Required)](actions/list-calendar-appointments-session-required.md) | `GET /calendar/appointment` |  |
| [List Calendar Projects (Session Required)](actions/list-calendar-projects-session-required.md) | `GET /calendar/project` |  |
| [List Calendars (Session Required)](actions/list-calendars-session-required.md) | `GET /calendar` |  |
| [List Form Templates (Session Required)](actions/list-form-templates-session-required.md) | `GET /form/template` |  |
| [List Forms (Session Required)](actions/list-forms-session-required.md) | `GET /form` |  |
| [List Lead Status Funnel Leads (Session Required)](actions/list-lead-status-funnel-leads-session-required.md) | `GET /leadstatus/funnel/leads/all` |  |
| [List Projects (Session Required)](actions/list-projects-session-required.md) | `GET /project` |  |
| [List Scheduler Dropdown Options (Session Required)](actions/list-scheduler-dropdown-options-session-required.md) | `GET /scheduler/dropdown/list` |  |
| [List Schedulers (Session Required)](actions/list-schedulers-session-required.md) | `GET /scheduler` |  |
| [List Workflow Templates (Session Required)](actions/list-workflow-templates-session-required.md) | `GET /workflow/template` |  |
| [Validate Zapier API Key](actions/validate-zapier-api-key.md) | `GET /zapier/key` | [docs](https://help.dubsado.com/en/articles/909872-connecting-with-zapier) |
