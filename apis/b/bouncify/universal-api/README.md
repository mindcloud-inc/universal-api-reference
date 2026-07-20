# <img src="https://images.mindcloud.co/apps/icons/0x0_1780952846886.png" alt="Bouncify logo" width="28" height="28"> Bouncify: Universal API

Verify individual emails, upload and manage Bouncify bulk verification jobs, and download bulk verification results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bouncify/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bouncify.io
- **Vendor API docs:** https://bouncify.io/docs/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bouncify/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Account Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves credit balance information from Bouncify. |

### Bulk Job Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Job Status](actions/check-job-status.md) | GET | Retrieves bulk email list job status from Bouncify. |

### Bulk Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Bulk Email List](actions/delete-bulk-email-list.md) | DELETE | Deletes a bulk email list from Bouncify. |
| [Start Verifying Bulk List](actions/start-verifying-bulk-list.md) | PUT | Starts verifying a bulk email list in Bouncify. |
| [Upload Bulk Email List](actions/upload-bulk-email-list.md) | POST | Uploads a bulk email list to Bouncify. |

### Bulk Verification Result

| Action | Method | Description |
| --- | --- | --- |
| [Download Verification Result](actions/download-verification-result.md) | GET | Downloads a bulk verification result from Bouncify. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with Bouncify. |

