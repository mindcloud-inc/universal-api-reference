# Loqate: Native API Reference

A consolidated summary of Loqate's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.loqate.com/api-reference
- **API base URL:** `https://api.addressy.com`

## Authentication

### API Key

Create a generic Loqate API key in account.loqate.com, then paste it here.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.loqate.com/api-reference/address-capture/quickstart)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `items`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Validate Bank Accounts](actions/batch-validate-bank-accounts.md) | `GET /BankAccountValidation/Batch/Validate/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/bank-validation/batch) |
| [Batch Validate Emails](actions/batch-validate-emails.md) | `GET /EmailValidation/Batch/Validate/v1.20/json6.ws` | [docs](https://docs.loqate.com/api-reference/email-validation/batch-validate) |
| [Detect Country From IP Address](actions/detect-country-from-ip-address.md) | `GET /Extras/Web/Ip2Country/v1.10/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/ip2country/ip2country) |
| [Find Addresses](actions/find-addresses.md) | `GET /Capture/Interactive/Find/v1.20/json6.ws` | [docs](https://docs.loqate.com/api-reference/address-capture/find) |
| [Find Nearby International Places](actions/find-nearby-international-places.md) | `GET /Geocoding/International/RetrieveNearestPlaces/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/international-retrievenearestplaces) |
| [Find Nearby UK Places](actions/find-nearby-uk-places.md) | `GET /Geocoding/UK/RetrieveNearestPlaces/v1.20/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/uk-retrievenearestplaces) |
| [Find UK Location](actions/find-uk-location.md) | `GET /Geocoding/UK/Find/v2.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/uk-find) |
| [Geocode International Location](actions/geocode-international-location.md) | `GET /Geocoding/International/Geocode/v1.10/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/international-geocode) |
| [Geocode UK Location](actions/geocode-uk-location.md) | `GET /Geocoding/UK/Geocode/v2.10/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/uk-geocode) |
| [Get Country From Coordinates](actions/get-country-from-coordinates.md) | `GET /Geocoding/International/PositionToCountry/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/international-positiontocountry) |
| [Get Directions](actions/get-directions.md) | `GET /DistancesAndDirections/Interactive/Directions/v2.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/distances-and-directions/directions) |
| [Get Distance](actions/get-distance.md) | `GET /DistancesAndDirections/Interactive/Distance/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/distances-and-directions/distance) |
| [Lookup UK Government Data By Postcode](actions/lookup-uk-government-data-by-postcode.md) | `GET /GovernmentData/Postzon/RetrieveByPostcode/v1.50/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/governmentdata/postzon-retrievebypostcode) |
| [Retrieve Address](actions/retrieve-address.md) | `GET /Capture/Interactive/Retrieve/v1.30/json6.ws` | [docs](https://docs.loqate.com/api-reference/address-capture/retrieve) |
| [Retrieve Bank Branch By Sort Code](actions/retrieve-bank-branch-by-sort-code.md) | `GET /BankAccountValidation/Interactive/RetrieveBySortcode/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/bank-validation/retrievebysortcode) |
| [Reverse Geocode International Coordinates](actions/reverse-geocode-international-coordinates.md) | `GET /Geocoding/International/ReverseGeocode/v2.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/geocode/geocoding/international-reversegeocode) |
| [Validate Bank Account](actions/validate-bank-account.md) | `GET /BankAccountValidation/Interactive/Validate/v2.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/bank-validation/individual) |
| [Validate Email](actions/validate-email.md) | `GET /EmailValidation/Interactive/Validate/v2.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/email-validation/individual) |
| [Validate International Bank Account](actions/validate-international-bank-account.md) | `GET /InternationalBankValidation/Interactive/Validate/v1.00/json6.ws` | [docs](https://docs.loqate.com/api-reference/bank-validation/international) |
| [Validate Phone](actions/validate-phone.md) | `GET /PhoneNumberValidation/Interactive/Validate/v2.20/json6.ws` | [docs](https://docs.loqate.com/api-reference/phone-validation/individual-validate) |
