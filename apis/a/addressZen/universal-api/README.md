# <img src="https://images.mindcloud.co/apps/icons/clip-path-group_1780945465717.png" alt="AddressZen logo" width="28" height="28"> AddressZen: Universal API

AddressZen: Search, verify, and standardize addresses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/addressZen/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://addresszen.com
- **Vendor API docs:** https://docs.addresszen.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Email Validation](actions/email-validation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation?connectionId=$CONNECTION_ID&query=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Email Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Email Validation](actions/email-validation.md) | GET | Retrieves email validation details from AddressZen. |

### Phone Number Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Phone Number Validation](actions/phone-number-validation.md) | GET | Retrieves phone number validation details from AddressZen. |

