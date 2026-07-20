# <img src="https://images.mindcloud.co/apps/icons/whats-app-number-validator_1776106792836.png" alt="WhatsApp Number Validator logo" width="28" height="28"> WhatsApp Number Validator: Universal API

Validate WhatsApp numbers and confirm active accounts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whatsAppNumberValidator/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zylalabs.com/api-marketplace/communication%2B%26%2Bmessaging/whatsapp%2Bnumber%2Bvalidator%2Bapi/9470
- **Vendor API docs:** https://zylalabs.com/api-marketplace/communication%2B%26%2Bmessaging/whatsapp%2Bnumber%2Bvalidator%2Bapi/9470

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate WhatsApp Number](actions/validate-whats-app-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsAppNumberValidator/latest/actions/validate-whats-app-number?connectionId=$CONNECTION_ID&number=14083742784" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Validate WhatsApp Number](actions/validate-whats-app-number.md) | GET | Retrieves WhatsApp number validation details from WhatsApp Number Validator. |

