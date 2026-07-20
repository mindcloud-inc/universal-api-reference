# <img src="https://images.mindcloud.co/apps/icons/quick-email-verification_1773781776801.png" alt="QuickEmailVerification logo" width="28" height="28"> QuickEmailVerification: Universal API

Email verification and bulk email list validation API for real-time checks, sandbox testing, and asynchronous verification jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quickEmailVerification/latest
- **Category:** Communication / Email Communications
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quickemailverification.com
- **Vendor API docs:** https://docs.quickemailverification.com/email-verification-api/kick-start-with-email-validation-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email in Sandbox Mode](actions/verify-email-in-sandbox-mode.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode?connectionId=$CONNECTION_ID&email=safe-to-send%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves an email verification result from QuickEmailVerification. |
| [Verify Email in Sandbox Mode](actions/verify-email-in-sandbox-mode.md) | GET | Retrieves a simulated email verification result from QuickEmailVerification. |

