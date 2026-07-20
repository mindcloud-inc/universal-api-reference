# <img src="https://images.mindcloud.co/apps/icons/mailsso_1774393803460.png" alt="mails.so logo" width="28" height="28"> mails.so: Universal API

Validate email addresses and retrieve async bulk validation results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailsso/latest
- **Category:** Communication / Email Communications
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mails.so
- **Vendor API docs:** https://docs.mails.so/intro/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Email](actions/validate-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Batch Validation Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch Validation Job](actions/create-batch-validation-job.md) | POST | Creates a new batch validation job in mails.so. |
| [Retrieve Batch Validation Job](actions/retrieve-batch-validation-job.md) | GET | Retrieves a batch validation job from mails.so. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Retrieves email validation results from mails.so. |

