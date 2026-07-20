# <img src="https://images.mindcloud.co/apps/icons/2023-07-31_1776264581982.png" alt="Email List Validation logo" width="28" height="28"> Email List Validation: Universal API

Email List Validation verifies email addresses and returns deliverability results for list hygiene and signup validation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailListValidation/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emaillistvalidation.com/
- **Vendor API docs:** https://help.emaillistvalidation.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email Address](actions/verify-email-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListValidation/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email Address](actions/verify-email-address.md) | GET |  |

