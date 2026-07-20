# AbcSubmit: Native API Reference

A consolidated summary of AbcSubmit's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.abcsubmit.com/site/api-documentation/
- **API base URL:** `https://www.abcsubmit.com`

## Authentication

### JWT Login (Username + Password)

Sign in with your AbcSubmit username or email and password.

### Credentials

- **Username:** `username` · required · Email address or username used to sign in to AbcSubmit.

Send these headers with each API request:

```http
jwt: <custom.accessToken>
```

[Official authentication documentation](https://www.abcsubmit.com/site/api-documentation/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Password](actions/change-password.md) | `POST /api/v1/users/change-password` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Create Account](actions/create-account.md) | `POST /api/v1/users/create-account` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Export Submissions](actions/export-submissions.md) | `POST /api/v1/submissions/:form_id/export/:format` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Forgot Password](actions/forgot-password.md) | `POST /api/v1/users/forgot-password` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get Form Document](actions/get-form-document.md) | `GET /api/v1/forms/:form_id` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get Form JS Embed Code](actions/get-form-js-embed-code.md) | `GET /embed/:form_id/:seo_form_name.js` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get Form Template Document](actions/get-form-template-document.md) | `GET /api/v1/templates/:form_id` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get My Plan](actions/get-my-plan.md) | `GET /api/v1/users/my-plan` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get My Stats](actions/get-my-stats.md) | `GET /api/v1/users/my-stats` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get My Upgrade Plans](actions/get-my-upgrade-plans.md) | `GET /api/v1/users/my-upgrade-plans` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get Submissions](actions/get-submissions.md) | `GET /api/v1/submissions/:form_id` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Get Submissions Count](actions/get-submissions-count.md) | `GET /api/v1/submissions/:form_id/count` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [List Form Templates](actions/list-form-templates.md) | `GET /api/v1/templates` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [List Forms](actions/list-forms.md) | `GET /api/v1/forms/` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [List Plans](actions/list-plans.md) | `GET /api/v1/users/plans` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
| [Login](actions/login.md) | `POST /api/v1/users/login` | [docs](https://www.abcsubmit.com/site/api-documentation/) |
