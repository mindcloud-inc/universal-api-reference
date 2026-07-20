# <img src="https://images.mindcloud.co/apps/icons/validto-icon_1774989422131.png" alt="validTo logo" width="28" height="28"> validTo: Universal API

Validate email addresses and manage bulk verification lists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/validTo/latest
- **Category:** Communication / Email Communications
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://validto.com/
- **Vendor API docs:** https://validto.readme.io/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validTo/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Bulk Validation List

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Validation List](actions/create-bulk-validation-list.md) | POST | Creates a bulk validation list in validTo. |
| [Delete Bulk Validation List](actions/delete-bulk-validation-list.md) | DELETE | Deletes a bulk validation list from validTo. |
| [Get Bulk Validation Progress](actions/get-bulk-validation-progress.md) | GET | Retrieves bulk validation progress from validTo. |
| [Start Bulk Validation](actions/start-bulk-validation.md) | PUT | Starts a bulk validation list in validTo. |

### Bulk Validation Results

| Action | Method | Description |
| --- | --- | --- |
| [Download Bulk Validation Results](actions/download-bulk-validation-results.md) | GET | Retrieves bulk validation results from validTo. |

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves your credit balance from validTo. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email Address](actions/verify-email-address.md) | GET | Verifies an email address with validTo. |

