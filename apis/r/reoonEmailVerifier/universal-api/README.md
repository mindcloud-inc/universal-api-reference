# <img src="https://images.mindcloud.co/apps/icons/reoon-email-verifier_1775853214275.png" alt="Reoon Email Verifier logo" width="28" height="28"> Reoon Email Verifier: Universal API

Verify single emails or bulk email lists with Reoon Email Verifier. Supports quick and power verification, bulk task creation and result retrieval, and account balance checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reoonEmailVerifier/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emailverifier.reoon.com/
- **Vendor API docs:** https://www.reoon.com/articles/api-documentation-of-reoon-email-verifier/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Account Balance](actions/check-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Check Account Balance](actions/check-account-balance.md) | GET |  |
| [Verify Email Power](actions/verify-email-power.md) | GET |  |
| [Verify Email Quick](actions/verify-email-quick.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Verification Task](actions/create-bulk-verification-task.md) | POST |  |
| [Get Bulk Verification Task Result](actions/get-bulk-verification-task-result.md) | GET |  |

