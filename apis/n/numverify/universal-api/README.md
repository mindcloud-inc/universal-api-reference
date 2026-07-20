# <img src="https://images.mindcloud.co/apps/icons/numverify-shortcut-icon-3_1774294122887.png" alt="Numverify logo" width="28" height="28"> Numverify: Universal API

Validate phone numbers and list supported countries worldwide

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/numverify/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://numverify.com
- **Vendor API docs:** https://docs.apilayer.com/numverify/docs/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Countries](actions/list-supported-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numverify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Countries](actions/list-supported-countries.md) | GET | Retrieves supported countries and dialing codes from Numverify. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Retrieves validation details for a phone number from Numverify. |

