# <img src="https://images.mindcloud.co/apps/icons/emailable_1774029572462.png" alt="Emailable logo" width="28" height="28"> Emailable: Universal API

Email verification platform for validating individual and batch email addresses and checking account credit availability.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailable/latest
- **Category:** Communication / Email Communications
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://emailable.com
- **Vendor API docs:** https://emailable.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailable/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account information from Emailable. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address in Emailable. |

### Verification Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Verification Batch](actions/create-verification-batch.md) | POST | Creates an email verification batch in Emailable. |
| [Get Batch Status](actions/get-batch-status.md) | GET | Retrieves the status of a batch from Emailable. |

