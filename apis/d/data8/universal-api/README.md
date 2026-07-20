# <img src="https://images.mindcloud.co/apps/icons/data8_1774631478379.png" alt="Data8 logo" width="28" height="28"> Data8: Universal API

Validate, cleanse, and enrich address, email, phone, location, name, country, and bank data with Data8 web services.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/data8/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.data-8.co.uk
- **Vendor API docs:** https://docs.data-8.co.uk/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Bank Account](actions/validate-bank-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-bank-account?connectionId=$CONNECTION_ID&sortCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Address](actions/fetch-address.md) | GET | Retrieves an address from Data8 by address key. |
| [Find Address](actions/find-address.md) | GET | Finds addresses in Data8 by town or street. |
| [Find Addresses by Locality Key](actions/find-addresses-by-locality-key.md) | GET | Finds addresses in Data8 by locality key. |
| [Find Addresses by Street Key](actions/find-addresses-by-street-key.md) | GET | Finds addresses in Data8 by street key. |
| [Find Full Address](actions/find-full-address.md) | GET | Finds full address details in Data8 by town or street. |
| [Find Localities by Name](actions/find-localities-by-name.md) | GET | Finds localities in Data8 by name. |
| [Find Localities by Postcode](actions/find-localities-by-postcode.md) | GET | Finds localities in Data8 by postcode. |
| [Find Streets by Locality Key](actions/find-streets-by-locality-key.md) | GET | Finds streets in Data8 by locality key. |
| [Find Streets by Name](actions/find-streets-by-name.md) | GET | Finds streets in Data8 by locality name. |
| [Get Full Address](actions/get-full-address.md) | GET | Retrieves a full address from Data8 by postcode. |
| [Validate Postcode](actions/validate-postcode.md) | GET | Validates a submitted postcode with Data8. |

### Bank Account

| Action | Method | Description |
| --- | --- | --- |
| [Validate Bank Account](actions/validate-bank-account.md) | GET | Validates a bank account with Data8. |
| [Validate IBAN](actions/validate-iban.md) | GET | Validates a submitted IBAN with Data8. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Detect Country](actions/detect-country.md) | GET | Detects a country from contact data in Data8. |
| [Detect Country from IP Address](actions/detect-country-from-ip-address.md) | GET | Detects a country from an IP address in Data8. |

### Email Address

| Action | Method | Description |
| --- | --- | --- |
| [Cleanse Email Address](actions/cleanse-email-address.md) | GET | Cleanses an email address with Data8. |
| [Validate Email Address](actions/validate-email-address.md) | GET | Validates an email address with Data8. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Towns](actions/autocomplete-towns.md) | GET | Finds town name suggestions in Data8. |
| [Find Location](actions/find-location.md) | GET | Finds location details in Data8 by postcode. |
| [Find Nearest Location](actions/find-nearest-location.md) | GET | Finds the nearest location in Data8. |
| [Geocode Address](actions/geocode-address.md) | GET | Geocodes a submitted address with Data8. |

### Name

| Action | Method | Description |
| --- | --- | --- |
| [Clean Name](actions/clean-name.md) | GET | Cleanses a submitted name with Data8. |
| [Parse Name](actions/parse-name.md) | GET | Parses a submitted name with Data8. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Validates a phone number with Data8. |

