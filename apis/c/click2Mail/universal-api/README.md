# <img src="https://images.mindcloud.co/apps/icons/click2mail_1774386868212.png" alt="Click2Mail logo" width="28" height="28"> Click2Mail: Universal API

Manage Click2Mail addresses, documents, proofs, cost estimates, and mail jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/click2Mail/latest
- **Category:** Communication / Team Messaging
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developers.click2mail.com/
- **Vendor API docs:** https://developers.click2mail.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Credit Balance](actions/check-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/check-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Address](actions/create-account-address.md) | POST | Creates a new account address in Click2Mail. |
| [List Account Addresses](actions/list-account-addresses.md) | GET | Retrieves a list of account addresses from Click2Mail. |
| [Update Account Address](actions/update-account-address.md) | PUT | Updates an existing account address in Click2Mail. |

### Address Book

| Action | Method | Description |
| --- | --- | --- |
| [Add Address Book Addresses](actions/add-address-book-addresses.md) | POST | Adds addresses to a Click2Mail address book. |
| [Create Address Book](actions/create-address-book.md) | POST | Creates a new address book in Click2Mail. |
| [Delete Address Book](actions/delete-address-book.md) | DELETE | Deletes an address book from Click2Mail. |
| [Get Address Book](actions/get-address-book.md) | GET | Retrieves an address book from Click2Mail. |
| [List Address Books](actions/list-address-books.md) | GET | Retrieves a list of address books from Click2Mail. |
| [Update Address Book Addresses](actions/update-address-book-addresses.md) | PUT | Updates addresses in a Click2Mail address book. |

### Address List

| Action | Method | Description |
| --- | --- | --- |
| [Add Address List Addresses](actions/add-address-list-addresses.md) | POST | Adds addresses to a Click2Mail address list. |
| [Add Addresses From Address Book](actions/add-addresses-from-address-book.md) | POST | Adds address book addresses to a Click2Mail address list. |
| [Add Addresses To Mailing List](actions/add-addresses-to-mailing-list.md) | POST | Adds addresses to a Click2Mail mailing list. |
| [Check Address List Name](actions/check-address-list-name.md) | GET | Checks whether an address list name is available in Click2Mail. |
| [Create Address List](actions/create-address-list.md) | POST | Creates a new address list in Click2Mail. |
| [Delete Address List](actions/delete-address-list.md) | DELETE | Deletes an address list from Click2Mail. |
| [Delete Addresses From List](actions/delete-addresses-from-list.md) | DELETE | Deletes addresses from a Click2Mail list. |
| [Get Address List](actions/get-address-list.md) | GET | Retrieves an address list from Click2Mail. |
| [Get Address List Info](actions/get-address-list-info.md) | GET | Retrieves address list metadata from Click2Mail. |
| [List Address Lists](actions/list-address-lists.md) | GET | Retrieves a list of address lists from Click2Mail. |
| [Update Address List Addresses](actions/update-address-list-addresses.md) | PUT | Updates addresses in a Click2Mail address list. |

### Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Cost Estimate](actions/get-cost-estimate.md) | GET | Retrieves a mailing cost estimate from Click2Mail. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Credit Balance](actions/check-credit-balance.md) | GET | Retrieves the credit balance from Click2Mail. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Check Document Name](actions/check-document-name.md) | GET | Checks whether a document name is available in Click2Mail. |
| [Convert Document To PDF](actions/convert-document-to-pdf.md) | POST | Creates a PDF document in Click2Mail. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Click2Mail. |
| [Create Document From URL](actions/create-document-from-url.md) | POST | Creates a document in Click2Mail from a URL. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from Click2Mail. |
| [Merge Document](actions/merge-document.md) | POST | Creates a merged document in Click2Mail. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Click2Mail. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job record from Click2Mail. |
| [Get Job Cost](actions/get-job-cost.md) | GET | Retrieves job cost details from Click2Mail. |
| [Get Job Info](actions/get-job-info.md) | GET | Retrieves detailed job information from Click2Mail. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves a list of jobs from Click2Mail. |
| [Submit Job](actions/submit-job.md) | PUT | Submits an existing job in Click2Mail. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in Click2Mail. |

### Job Document

| Action | Method | Description |
| --- | --- | --- |
| [List Job Documents](actions/list-job-documents.md) | GET | Retrieves a list of job documents from Click2Mail. |

### Proof

| Action | Method | Description |
| --- | --- | --- |
| [Accept Proof](actions/accept-proof.md) | PUT | Accepts a proof for a Click2Mail job. |
| [Create Proof](actions/create-proof.md) | POST | Creates a proof for a Click2Mail job. |
| [Get Proof](actions/get-proof.md) | GET | Retrieves a proof file from Click2Mail. |

### Variable Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Variable Data](actions/get-document-variable-data.md) | GET | Retrieves variable data for a Click2Mail document. |

