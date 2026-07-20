# <img src="https://images.mindcloud.co/apps/icons/listclean-icon_1778078672922.png" alt="Listclean logo" width="28" height="28"> Listclean: Universal API

Listclean helps validate individual email addresses, verify email batches, manage uploaded verification lists, download list-cleaning results, and monitor account credits through its REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/listclean/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://listclean.xyz/
- **Vendor API docs:** https://api.listclean.xyz/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Remaining Credits](actions/get-remaining-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-remaining-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Profile](actions/get-account-profile.md) | GET | Retrieves account profile details from Listclean. |
| [Update Account Profile](actions/update-account-profile.md) | PUT | Updates account profile details in Listclean. |

### Batch Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Batch Of Emails](actions/verify-batch-of-emails.md) | POST | Verifies up to 3,000 email addresses in Listclean. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Remaining Credits](actions/get-remaining-credits.md) | GET | Retrieves remaining account credits from Listclean. |

### Csv Upload

| Action | Method | Description |
| --- | --- | --- |
| [List CSV Uploads](actions/list-csv-uploads.md) | GET | Retrieves saved CSV uploads from Listclean. |
| [Start Upload](actions/start-upload.md) | POST | Starts a CSV upload in Listclean. |

### Csv Upload Chunk

| Action | Method | Description |
| --- | --- | --- |
| [Upload Chunk](actions/upload-chunk.md) | PUT | Uploads a CSV chunk to Listclean. |

### Csv Upload Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload Status](actions/get-upload-status.md) | GET | Retrieves CSV upload status from Listclean. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email Address](actions/verify-email-address.md) | GET | Retrieves an email verification result from Listclean. |

### List Results Csv

| Action | Method | Description |
| --- | --- | --- |
| [Download List Results As CSV](actions/download-list-results-as-csv.md) | GET | Retrieves verification list results as a CSV file from Listclean. |

### List Results Json

| Action | Method | Description |
| --- | --- | --- |
| [Download List Results As JSON](actions/download-list-results-as-json.md) | GET | Retrieves verification list results as JSON from Listclean. |

### Verification List

| Action | Method | Description |
| --- | --- | --- |
| [Delete List](actions/delete-list.md) | DELETE | Deletes a verification list from Listclean. |
| [Get List Information](actions/get-list-information.md) | GET | Retrieves verification list details from Listclean. |
| [List All Verification Lists](actions/list-all-verification-lists.md) | GET | Retrieves all verification lists from Listclean. |

### Verification Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Logs](actions/get-verification-logs.md) | GET | Retrieves email verification logs from Listclean. |

