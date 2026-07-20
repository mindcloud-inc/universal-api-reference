# <img src="https://images.mindcloud.co/apps/icons/email-verifier-api_1776258276382.png" alt="Email Verifier Api logo" width="28" height="28"> Email Verifier Api: Universal API

Real-time email verification and enrichment against Email Verifier API v2.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailVerifierApi/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emailverifierapi.com/
- **Vendor API docs:** https://emailverifierapi.com/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email (GET)](actions/verify-email-get.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email (GET)](actions/verify-email-get.md) | GET |  |
| [Verify Email (POST)](actions/verify-email-post.md) | POST |  |

