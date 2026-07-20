# <img src="https://images.mindcloud.co/apps/icons/toofr_1776790044210.png" alt="Toofr logo" width="28" height="28"> Toofr: Universal API

Toofr, now FindEmails, provides email discovery, verification, company-domain lookup, list management, and prospect enrichment APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/toofr/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.findemails.com
- **Vendor API docs:** https://developer.findemails.com/?from=explinks.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Domain](actions/get-company-domain.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-company-domain?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bulk Email List Record Job

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Email List Records](actions/bulk-create-email-list-records.md) | POST | Creates multiple email list records in Toofr. |

### Company Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Company](actions/classify-company.md) | GET | Retrieves company classification details from Toofr. |

### Company Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Domain](actions/get-company-domain.md) | GET | Retrieves a company's domain from Toofr. |

### Company Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Prospects](actions/get-company-prospects.md) | GET | Retrieves prospects for a company from Toofr. |

### Company Prospect List

| Action | Method | Description |
| --- | --- | --- |
| [Create Company Prospect List](actions/create-company-prospect-list.md) | POST | Creates a company prospect list in Toofr. |

### Email Guess

| Action | Method | Description |
| --- | --- | --- |
| [Guess Email](actions/guess-email.md) | GET | Guesses a prospect's email address in Toofr. |
| [Queue Email Guess](actions/queue-email-guess.md) | POST | Queues an email guess in Toofr for callback delivery. |

### Email List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List](actions/create-email-list.md) | POST | Creates a new email list in Toofr. |
| [Get Email List](actions/get-email-list.md) | GET | Retrieves an email list from Toofr. |
| [List Marketplace Email Lists](actions/list-marketplace-email-lists.md) | GET | Retrieves marketplace email lists from Toofr. |
| [List Owned Email Lists](actions/list-owned-email-lists.md) | GET | Retrieves owned email lists from Toofr. |

### Email List Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Email List Record](actions/create-email-list-record.md) | POST | Creates a new email list record in Toofr. |
| [Get Email List Record](actions/get-email-list-record.md) | GET | Retrieves an email list record from Toofr. |
| [List Email List Records](actions/list-email-list-records.md) | GET | Retrieves email list records from a Toofr list. |

### Email List Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Marketplace Email Lists](actions/search-marketplace-email-lists.md) | GET | Finds marketplace email lists in Toofr by search query. |
| [Search Owned Email Lists](actions/search-owned-email-lists.md) | GET | Finds owned email lists in Toofr by search query. |

### Email Pattern List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Pattern List](actions/create-email-pattern-list.md) | POST | Creates an email pattern list in Toofr. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Queues an email verification in Toofr for callback delivery. |

### Email Verification List

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Verification List](actions/create-email-verification-list.md) | POST | Creates an email verification list in Toofr. |

### Guess All Processing List

| Action | Method | Description |
| --- | --- | --- |
| [Create Guess All Processing List](actions/create-guess-all-processing-list.md) | POST | Creates a guess-all processing list in Toofr. |

### Guess Processing List

| Action | Method | Description |
| --- | --- | --- |
| [Create Guess Processing List](actions/create-guess-processing-list.md) | POST | Creates a guess processing list in Toofr. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Find Prospects](actions/find-prospects.md) | GET | Finds prospects in Toofr by title or company. |

### Prospect Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Prospect Profile](actions/get-prospect-profile.md) | GET | Retrieves a prospect profile from Toofr. |

### Purchased Email List

| Action | Method | Description |
| --- | --- | --- |
| [Purchase Marketplace List](actions/purchase-marketplace-list.md) | POST | Purchases a marketplace email list in Toofr. |

