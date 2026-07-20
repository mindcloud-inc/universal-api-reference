# <img src="https://images.mindcloud.co/apps/icons/verify550_1774906451994.png" alt="Verify550 logo" width="28" height="28"> Verify550: Universal API

Verify emails, validate lists, and export verification results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/verify550/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://verify550.com
- **Vendor API docs:** https://verify550.com/documentation/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Single Email](actions/verify-single-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verify550/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Verify Single Email](actions/verify-single-email.md) | GET | Verifies a single email address with Verify550. |

### Export Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Download Verification Results](actions/download-verification-results.md) | GET | Downloads verification result files from Verify550. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Processed File](actions/download-processed-file.md) | GET | Downloads a processed file from Verify550. |
| [Download Ready File](actions/download-ready-file.md) | GET | Downloads a ready verification file from Verify550. |
| [Upload Bulk Email File](actions/upload-bulk-email-file.md) | POST | Uploads a bulk email file to Verify550. |
| [Upload Bulk Phone File](actions/upload-bulk-phone-file.md) | POST | Uploads a bulk phone file to Verify550. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Job](actions/get-verification-job.md) | GET | Retrieves a verification job from Verify550. |

