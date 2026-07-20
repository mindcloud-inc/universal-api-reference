# <img src="https://images.mindcloud.co/apps/icons/ideal-postcodes_1774361762759.png" alt="Ideal Postcodes logo" width="28" height="28"> Ideal Postcodes: Universal API

Search, validate, and manage addresses, places, emails, and phone numbers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/idealPostcodes/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ideal-postcodes.co.uk
- **Vendor API docs:** https://docs.ideal-postcodes.co.uk/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Postcode](actions/lookup-postcode.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/lookup-postcode?connectionId=$CONNECTION_ID&postcode=SW1A%202AA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Cleanse Address](actions/cleanse-address.md) | GET | Finds the closest matching address in Ideal Postcodes. |
| [Extract Addresses](actions/extract-addresses.md) | GET | Finds addresses in Ideal Postcodes by text query. |
| [Find Address](actions/find-address.md) | GET | Finds address suggestions in Ideal Postcodes by text query. |
| [Resolve Address](actions/resolve-address.md) | GET | Retrieves a UK address from Ideal Postcodes by address ID. |
| [Retrieve Address](actions/retrieve-address.md) | GET | Retrieves a US address from Ideal Postcodes by address ID. |
| [Retrieve by UDPRN](actions/retrieve-by-udprn.md) | GET | Retrieves an address from Ideal Postcodes by UDPRN. |
| [Retrieve by UMPRN](actions/retrieve-by-umprn.md) | GET | Retrieves a multiple occupancy address from Ideal Postcodes by UMPRN. |
| [Verify Address](actions/verify-address.md) | GET | Verifies and standardizes a US address in Ideal Postcodes. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Email Validation](actions/email-validation.md) | GET | Validates an email address in Ideal Postcodes. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Phone Number Validation](actions/phone-number-validation.md) | GET | Validates a phone number in Ideal Postcodes. |

### Place

| Action | Method | Description |
| --- | --- | --- |
| [Find Place](actions/find-place.md) | GET | Finds place suggestions in Ideal Postcodes by text query. |
| [Resolve Place](actions/resolve-place.md) | GET | Retrieves a place from Ideal Postcodes by place ID. |

### Postcode

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Postcode](actions/lookup-postcode.md) | GET | Retrieves addresses from Ideal Postcodes for a UK postcode. |

