# <img src="https://images.mindcloud.co/apps/icons/favicon-api-emaillistverify-com-48x48_1778269352551.png" alt="EmailListVerify logo" width="28" height="28"> EmailListVerify: Universal API

EmailListVerify validates email deliverability, checks disposable domains and blacklists, finds business contacts, manages bulk verification jobs, checks inbox placement tests, and reports account credits through its documented REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailListVerify/latest
- **Category:** Marketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emaillistverify.com
- **Vendor API docs:** https://api.emaillistverify.com/api-doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Blacklist Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Blacklists](actions/check-blacklists.md) | GET | Checks IP or domain blacklists in EmailListVerify. |

### Contact Email

| Action | Method | Description |
| --- | --- | --- |
| [Find Contact Email](actions/find-contact-email.md) | GET | Finds a contact email in EmailListVerify by name or domain. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your available credits from EmailListVerify. |

### Disposable Domain Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Disposable Domain](actions/check-disposable-domain.md) | GET | Checks whether a domain is disposable in EmailListVerify. |

### Email List

| Action | Method | Description |
| --- | --- | --- |
| [Delete Email List](actions/delete-email-list.md) | DELETE | Deletes a finished email list from EmailListVerify. |
| [Get Email List Progress](actions/get-email-list-progress.md) | GET | Retrieves email list verification progress from EmailListVerify. |
| [Upload Email List](actions/upload-email-list.md) | POST | Uploads an email list for verification in EmailListVerify. |

### Email List Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Email List](actions/download-email-list.md) | GET | Downloads a finished email list from EmailListVerify. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves email deliverability status from EmailListVerify. |
| [Verify Email Detailed](actions/verify-email-detailed.md) | GET | Retrieves detailed email deliverability results from EmailListVerify. |

### Email Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Verification Job](actions/create-email-verification-job.md) | POST | Creates an asynchronous email verification job in EmailListVerify. |
| [Get Email Verification Job](actions/get-email-verification-job.md) | GET | Retrieves email verification job status and results from EmailListVerify. |

### Inbox Placement Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Placement Test](actions/create-inbox-placement-test.md) | POST | Creates an inbox placement test in EmailListVerify. |
| [Get Inbox Placement Test](actions/get-inbox-placement-test.md) | GET | Retrieves inbox placement test status and results from EmailListVerify. |

