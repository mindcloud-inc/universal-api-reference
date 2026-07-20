# <img src="https://images.mindcloud.co/apps/icons/kickbox_1773861998537.png" alt="Kickbox logo" width="28" height="28"> Kickbox: Universal API

Verify individual emails and batch email lists with Kickbox.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kickbox/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kickbox.com
- **Vendor API docs:** https://docs.kickbox.com/docs/api-overview-copy

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email](actions/verify-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Batch Verification Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Verification Status](actions/get-batch-verification-status.md) | GET | Retrieves a batch verification job from Kickbox. |
| [Start Batch Verification](actions/start-batch-verification.md) | POST | Starts a batch email verification job in Kickbox. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address with Kickbox. |

