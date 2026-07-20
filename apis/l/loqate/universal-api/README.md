# <img src="https://images.mindcloud.co/apps/icons/dfed75cf-1303-426b-9995-7286477317a1-0_1776441059933.png" alt="Loqate logo" width="28" height="28"> Loqate: Universal API

Find, validate, and retrieve addresses with Loqate

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loqate/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loqate.com/
- **Vendor API docs:** https://docs.loqate.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Find Addresses](actions/find-addresses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses?connectionId=$CONNECTION_ID&text=Loqate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Find Addresses](actions/find-addresses.md) | GET | Finds addresses in Loqate by search text. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Batch Validate Bank Accounts](actions/batch-validate-bank-accounts.md) | GET | Validates multiple bank accounts with Loqate. |
| [Batch Validate Emails](actions/batch-validate-emails.md) | GET | Validates multiple email addresses with Loqate. |
| [Detect Country From IP Address](actions/detect-country-from-ip-address.md) | GET | Detects a country from an IP address with Loqate. |
| [Find Nearby International Places](actions/find-nearby-international-places.md) | GET | Finds nearby international places with Loqate. |
| [Find Nearby UK Places](actions/find-nearby-uk-places.md) | GET | Finds nearby UK places with Loqate. |
| [Find UK Location](actions/find-uk-location.md) | GET | Finds a UK location with Loqate. |
| [Geocode International Location](actions/geocode-international-location.md) | GET | Geocodes an international location with Loqate. |
| [Geocode UK Location](actions/geocode-uk-location.md) | GET | Geocodes a UK location with Loqate. |
| [Get Country From Coordinates](actions/get-country-from-coordinates.md) | GET | Retrieves a country from coordinates with Loqate. |
| [Get Directions](actions/get-directions.md) | GET | Retrieves directions between locations from Loqate. |
| [Get Distance](actions/get-distance.md) | GET | Retrieves the distance between locations from Loqate. |
| [Lookup UK Government Data By Postcode](actions/lookup-uk-government-data-by-postcode.md) | GET | Retrieves UK government data from Loqate by postcode. |
| [Retrieve Address](actions/retrieve-address.md) | GET | Retrieves an address from Loqate. |
| [Retrieve Bank Branch By Sort Code](actions/retrieve-bank-branch-by-sort-code.md) | GET | Retrieves a bank branch from Loqate by sort code. |
| [Reverse Geocode International Coordinates](actions/reverse-geocode-international-coordinates.md) | GET | Reverse geocodes international coordinates with Loqate. |
| [Validate Bank Account](actions/validate-bank-account.md) | GET | Validates a bank account with Loqate. |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with Loqate. |
| [Validate International Bank Account](actions/validate-international-bank-account.md) | GET | Validates an international bank account with Loqate. |
| [Validate Phone](actions/validate-phone.md) | GET | Validates a phone number with Loqate. |

