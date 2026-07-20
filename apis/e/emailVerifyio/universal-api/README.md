# <img src="https://images.mindcloud.co/apps/icons/email-verifyio_1775146925526.png" alt="EmailVerify.io logo" width="28" height="28"> EmailVerify.io: Universal API

Verify single emails, launch bulk email verification tasks, fetch bulk verification results, check account credits, and find likely business email addresses through the documented EmailVerify.io API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailVerifyio/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emailverify.io/
- **Vendor API docs:** https://www.emailverify.io/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Email](actions/validate-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Account Balance](actions/check-account-balance.md) | GET | Retrieves account balance details from EmailVerify.io. |

### Bulk Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Verification Result](actions/get-bulk-verification-result.md) | GET | Retrieves a bulk verification task result from EmailVerify.io. |

### Bulk Verification Task

| Action | Method | Description |
| --- | --- | --- |
| [Start Bulk Verification Task](actions/start-bulk-verification-task.md) | POST | Creates a bulk verification task in EmailVerify.io. |

### Business Email Match

| Action | Method | Description |
| --- | --- | --- |
| [Find Business Email](actions/find-business-email.md) | GET | Finds a business email in EmailVerify.io by name and domain. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with EmailVerify.io. |

