# <img src="https://images.mindcloud.co/apps/icons/clearout_1774375888108.png" alt="Clearout logo" width="28" height="28"> Clearout: Universal API

Verify emails, find contacts, and enrich company domains with Clearout's REST API

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clearout/latest
- **Category:** Communication / Email Communications
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clearout.io
- **Vendor API docs:** https://docs.clearout.io/developers/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Available Credits](actions/get-available-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Reverse Lookup Domain](actions/reverse-lookup-domain.md) | GET | Retrieves company lead information from Clearout by domain. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Credits](actions/get-available-credits.md) | GET | Retrieves available credits from your Clearout account. |

### Domain Mx Record

| Action | Method | Description |
| --- | --- | --- |
| [Find MX Records](actions/find-mx-records.md) | GET | Retrieves MX records for a domain from Clearout. |

### Domain Whois

| Action | Method | Description |
| --- | --- | --- |
| [Find Whois](actions/find-whois.md) | GET | Retrieves Whois records for a domain from Clearout. |

### Email Finder Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Bulk Email Finder Batch](actions/cancel-bulk-email-finder-batch.md) | PUT | Cancels a running bulk email finder batch in Clearout. |
| [Create Bulk Email Finder Batch](actions/create-bulk-email-finder-batch.md) | POST | Creates a bulk email finder batch in Clearout. |
| [Download Bulk Email Finder Result](actions/download-bulk-email-finder-result.md) | GET | Retrieves a bulk email finder result download from Clearout. |
| [Get Bulk Email Finder Batch Status](actions/get-bulk-email-finder-batch-status.md) | GET | Retrieves bulk email finder batch status from Clearout. |
| [Remove Bulk Email Finder List](actions/remove-bulk-email-finder-list.md) | DELETE | Deletes a bulk email finder list from Clearout. |

### Email Finder Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Instant Email Finder Status](actions/get-instant-email-finder-status.md) | GET | Retrieves instant email finder queue status from Clearout. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Business Email](actions/verify-business-email.md) | GET | Retrieves business email verification results from Clearout. |
| [Verify Catch-All Email](actions/verify-catch-all-email.md) | GET | Retrieves catch-all email verification results from Clearout. |
| [Verify Disposable Email](actions/verify-disposable-email.md) | GET | Retrieves disposable email verification results from Clearout. |
| [Verify Email Instantly](actions/verify-email-instantly.md) | GET | Retrieves instant email verification results from Clearout. |
| [Verify Free Email](actions/verify-free-email.md) | GET | Retrieves free email verification results from Clearout. |
| [Verify Gibberish Email](actions/verify-gibberish-email.md) | GET | Retrieves gibberish email verification results from Clearout. |
| [Verify Role Email](actions/verify-role-email.md) | GET | Retrieves role email verification results from Clearout. |

### Email Verification Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Bulk Email Verification Batch](actions/cancel-bulk-email-verification-batch.md) | PUT | Cancels a running bulk email verification batch in Clearout. |
| [Create Bulk Email Verification Batch](actions/create-bulk-email-verification-batch.md) | POST | Creates a bulk email verification batch in Clearout. |
| [Delete Bulk Email Verification Result](actions/delete-bulk-email-verification-result.md) | DELETE | Deletes a bulk email verification result from Clearout. |
| [Download Bulk Email Verification Result](actions/download-bulk-email-verification-result.md) | GET | Retrieves a bulk email verification result download from Clearout. |
| [Get Bulk Email Verification Batch Status](actions/get-bulk-email-verification-batch-status.md) | GET | Retrieves bulk email verification batch status from Clearout. |

### Found Contact

| Action | Method | Description |
| --- | --- | --- |
| [Find Email Instantly](actions/find-email-instantly.md) | GET | Finds contact email addresses in Clearout instantly. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Reverse Lookup Email Address](actions/reverse-lookup-email-address.md) | GET | Retrieves lead information from Clearout by email address. |
| [Reverse Lookup LinkedIn Profile](actions/reverse-lookup-linked-in-profile.md) | GET | Retrieves lead information from Clearout by LinkedIn profile URL. |

