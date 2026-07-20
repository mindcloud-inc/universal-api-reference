# <img src="https://images.mindcloud.co/apps/icons/byteplant-address-validator_1775845572710.png" alt="Byteplant Address Validator logo" width="28" height="28"> Byteplant Address Validator: Universal API

Validate, autocomplete, geocode, and bulk-check postal addresses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/byteplantAddressValidator/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.byteplant.com/address-validator/
- **Vendor API docs:** https://www.byteplant.com/address-validator/api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Address](actions/verify-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address?connectionId=$CONNECTION_ID&streetAddress=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Details](actions/get-address-details.md) | GET | Retrieves address details from Byteplant Address Validator by suggestion ID. |
| [Verify Address](actions/verify-address.md) | GET | Retrieves address validation results from Byteplant Address Validator. |

### Address Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Search Address Suggestions](actions/search-address-suggestions.md) | GET | Finds address suggestions in Byteplant Address Validator. |

### Validation Task

| Action | Method | Description |
| --- | --- | --- |
| [Start Bulk Address Validation](actions/start-bulk-address-validation.md) | POST | Creates a bulk address validation task in Byteplant Address Validator. |

