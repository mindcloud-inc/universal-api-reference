# <img src="https://images.mindcloud.co/apps/icons/byteplant-email-validator_1774036092048.png" alt="Byteplant Email Validator logo" width="28" height="28"> Byteplant Email Validator: Universal API

Validate email addresses and detect disposable, fake, and mistyped emails

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/byteplantEmailValidator/latest
- **Category:** Communication / Email Communications
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.byteplant.com/email-validator/
- **Vendor API docs:** https://www.byteplant.com/email-validator/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email Address](actions/verify-email-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&emailAddress=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email Address](actions/verify-email-address.md) | GET | Retrieves email deliverability details from Byteplant Email Validator. |

### Validation Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Email Validation Task](actions/create-bulk-email-validation-task.md) | POST | Creates a bulk email validation task in Byteplant Email Validator. |

