# Get Website Report: Native API Reference

A consolidated summary of Get Website Report's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://app.getwebsite.report/login
- **API base URL:** `https://gwr-v3-prod-dot-turing-alcove-395007.el.r.appspot.com`

## Authentication

### Email & Password

Authenticate with a Get Website Report account email and password.

### Credentials

- **Email:** `email` · required
- **Password:** `password` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://app.getwebsite.report/login)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Consume License](actions/consume-license.md) | `POST /licenses/consume` | [docs](https://getwebsite.report/) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://app.getwebsite.report/) |
| [Get Report](actions/get-report.md) | `GET /reports/find` | [docs](https://app.getwebsite.report/audit/report/) |
| [Get Report Customization](actions/get-report-customization.md) | `GET /users/customization` | [docs](https://app.getwebsite.report/) |
| [List User Reports](actions/list-user-reports.md) | `GET /user_reports` | [docs](https://app.getwebsite.report/userReports) |
| [Log In with Google](actions/log-in-with-google.md) | `POST /google-login` | [docs](https://app.getwebsite.report/login) |
| [Login Account](actions/login-account.md) | `POST /login` | [docs](https://app.getwebsite.report/login) |
| [Reset Password](actions/reset-password.md) | `POST /users/reset-password` | [docs](https://app.getwebsite.report/reset-password) |
| [Send Password Reset Email](actions/send-password-reset-email.md) | `POST /users/forgot-password` | [docs](https://app.getwebsite.report/forgot-password) |
| [Sign Up Account](actions/sign-up-account.md) | `POST /signup` | [docs](https://app.getwebsite.report/login) |
| [Start Audit](actions/start-audit.md) | `POST /init-audit` | [docs](https://app.getwebsite.report/) |
| [Update Report Customization](actions/update-report-customization.md) | `POST /users/customization` | [docs](https://app.getwebsite.report/) |
| [Verify Email Token](actions/verify-email-token.md) | `GET /users/verify` | [docs](https://app.getwebsite.report/verify) |
| [Verify Reset Token](actions/verify-reset-token.md) | `GET /users/verify-reset` | [docs](https://app.getwebsite.report/reset-password) |
