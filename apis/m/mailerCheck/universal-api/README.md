# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1777051940862.png" alt="MailerCheck logo" width="28" height="28"> MailerCheck: Universal API

Verify email addresses and manage email verification lists.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailerCheck/latest
- **Category:** Communication / Email Communications
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailercheck.com/
- **Vendor API docs:** https://developers.mailercheck.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves current account details from MailerCheck. |

### Async Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Email Result](actions/get-async-email-result.md) | GET | Retrieves an asynchronous email verification result from MailerCheck. |
| [Verify Single Email Async](actions/verify-single-email-async.md) | POST | Creates an asynchronous email verification request in MailerCheck. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves account credit balance from MailerCheck. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Single Email](actions/verify-single-email.md) | GET | Retrieves a real-time email verification result from MailerCheck. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the current user from MailerCheck. |

### Verification List

| Action | Method | Description |
| --- | --- | --- |
| [Create Verification List](actions/create-verification-list.md) | POST | Creates a verification list in MailerCheck. |
| [Delete Verification List](actions/delete-verification-list.md) | DELETE | Deletes a verification list from MailerCheck. |
| [Get Verification List](actions/get-verification-list.md) | GET | Retrieves a verification list from MailerCheck. |
| [List Verification Lists](actions/list-verification-lists.md) | GET | Retrieves all verification lists from MailerCheck. |
| [Start List Verification](actions/start-list-verification.md) | PUT | Starts verification for a list in MailerCheck. |

### Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification List Results](actions/get-verification-list-results.md) | GET | Retrieves verification results for a list from MailerCheck. |

