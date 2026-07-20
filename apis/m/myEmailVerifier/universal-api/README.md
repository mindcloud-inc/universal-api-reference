# <img src="https://images.mindcloud.co/apps/icons/myemailverifier-client-apple-touch-icon_1775852873856.png" alt="MyEmailVerifier logo" width="28" height="28"> MyEmailVerifier: Universal API

Verify single email addresses, check remaining credits, and manage bulk verification jobs with MyEmailVerifier.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myEmailVerifier/latest
- **Category:** Marketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://myemailverifier.com
- **Vendor API docs:** https://myemailverifier.com/real-time-email-verification

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Bulk Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification File Info](actions/get-verification-file-info.md) | GET | Retrieves bulk verification job details from MyEmailVerifier. |

### Bulk Verification Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload Verification File](actions/upload-verification-file.md) | POST | Creates a bulk verification upload in MyEmailVerifier. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves remaining verification credits from MyEmailVerifier. |

### Email Analysis Result

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Email](actions/analyze-email.md) | GET | Analyzes an email address in MyEmailVerifier. |

### Email Analysis Service Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Analysis Status](actions/get-email-analysis-status.md) | GET | Retrieves email analysis service status from MyEmailVerifier. |

### Email Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Retrieves an email verification result from MyEmailVerifier by address. |

