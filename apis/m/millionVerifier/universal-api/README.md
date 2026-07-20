# <img src="https://images.mindcloud.co/apps/icons/id5bze8x-sq-1774635901315_1774635907782.png" alt="MillionVerifier logo" width="28" height="28"> MillionVerifier: Universal API

Verify emails, upload bulk lists, and download verification reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/millionVerifier/latest
- **Category:** Communication / Email Communications
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.millionverifier.com/
- **Vendor API docs:** https://developer.millionverifier.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Credits](actions/get-api-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Api Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get API Credits](actions/get-api-credits.md) | GET | Retrieves available API credits from MillionVerifier. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address in MillionVerifier. |

### Verification File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Verification File](actions/delete-verification-file.md) | DELETE | Deletes a verification file from MillionVerifier. |
| [Get Verification File](actions/get-verification-file.md) | GET | Retrieves a verification file from MillionVerifier. |
| [List Verification Files](actions/list-verification-files.md) | GET | Retrieves verification files from MillionVerifier. |
| [Stop Verification File](actions/stop-verification-file.md) | PUT | Stops a verification file in MillionVerifier. |
| [Upload Verification File](actions/upload-verification-file.md) | POST | Uploads a verification file to MillionVerifier. |

### Verification Report

| Action | Method | Description |
| --- | --- | --- |
| [Download Verification Report](actions/download-verification-report.md) | GET | Downloads a verification report from MillionVerifier. |

