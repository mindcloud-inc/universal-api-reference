# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-08-as-14_1775668710746.png" alt="Get Website Report logo" width="28" height="28"> Get Website Report: Universal API

Run website audits, retrieve generated reports, manage saved report customization, and perform account flows for Get Website Report.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/getWebsiteReport/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getwebsite.report
- **Vendor API docs:** https://app.getwebsite.report/login

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getWebsiteReport/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Consume License](actions/consume-license.md) | PUT |  |
| [Get Report](actions/get-report.md) | GET |  |
| [Get Report Customization](actions/get-report-customization.md) | GET |  |
| [List User Reports](actions/list-user-reports.md) | GET |  |
| [Log In with Google](actions/log-in-with-google.md) | POST |  |
| [Login Account](actions/login-account.md) | POST |  |
| [Reset Password](actions/reset-password.md) | PUT |  |
| [Send Password Reset Email](actions/send-password-reset-email.md) | POST |  |
| [Sign Up Account](actions/sign-up-account.md) | POST |  |
| [Start Audit](actions/start-audit.md) | POST |  |
| [Update Report Customization](actions/update-report-customization.md) | PUT |  |
| [Verify Email Token](actions/verify-email-token.md) | GET |  |
| [Verify Reset Token](actions/verify-reset-token.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

