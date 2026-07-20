# Data8: Native API Reference

A consolidated summary of Data8's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.data-8.co.uk/
- **API base URL:** `https://webservices.data-8.co.uk`

## Authentication

### API Key

Connect with a Data8 server-side API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.data-8.co.uk/authentication/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Towns](actions/autocomplete-towns.md) | `POST /Location/AutoCompleteTowns.json` | [docs](https://docs.data-8.co.uk/web-services/geocoding/autocompletetowns) |
| [Clean Name](actions/clean-name.md) | `POST /NameCleansing/CleanName.json` | [docs](https://docs.data-8.co.uk/web-services/namecleansing/cleanname) |
| [Cleanse Email Address](actions/cleanse-email-address.md) | `POST /EmailValidation/Cleanse.json` | [docs](https://docs.data-8.co.uk/web-services/emailvalidation/cleanse) |
| [Detect Country](actions/detect-country.md) | `POST /CountryDetection/DetectCountry.json` | [docs](https://docs.data-8.co.uk/web-services/countrydetection/detectcountry) |
| [Detect Country from IP Address](actions/detect-country-from-ip-address.md) | `POST /CountryDetection/IPAddressToCountrySimple.json` | [docs](https://docs.data-8.co.uk/web-services/countrydetection/ipaddresstocountrysimple) |
| [Fetch Address](actions/fetch-address.md) | `POST /AddressCapture/FetchAddress.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/fetchaddress) |
| [Find Address](actions/find-address.md) | `POST /AddressCapture/FindAddress.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/findaddress) |
| [Find Addresses by Locality Key](actions/find-addresses-by-locality-key.md) | `POST /AddressCapture/AddressesByLocalityKey.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/addressesbylocalitykey) |
| [Find Addresses by Street Key](actions/find-addresses-by-street-key.md) | `POST /AddressCapture/AddressesByStreetKey.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/addressesbystreetkey) |
| [Find Full Address](actions/find-full-address.md) | `POST /AddressCapture/FindFullAddress.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/findfulladdress) |
| [Find Localities by Name](actions/find-localities-by-name.md) | `POST /AddressCapture/LocalitiesByName.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/localitiesbyname) |
| [Find Localities by Postcode](actions/find-localities-by-postcode.md) | `POST /AddressCapture/LocalitiesByPostcode.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/localitiesbypostcode) |
| [Find Location](actions/find-location.md) | `POST /Location/FindLocation.json` | [docs](https://docs.data-8.co.uk/web-services/geocoding/findlocation) |
| [Find Nearest Location](actions/find-nearest-location.md) | `POST /Location/FindMyNearest.json` | [docs](https://docs.data-8.co.uk/web-services/geocoding/findmynearest) |
| [Find Streets by Locality Key](actions/find-streets-by-locality-key.md) | `POST /AddressCapture/StreetsByLocalityKey.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/streetsbylocalitykey) |
| [Find Streets by Name](actions/find-streets-by-name.md) | `POST /AddressCapture/StreetsByName.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/streetsbyname) |
| [Geocode Address](actions/geocode-address.md) | `POST /Location/Geocode.json` | [docs](https://docs.data-8.co.uk/web-services/geocoding/geocode) |
| [Get Full Address](actions/get-full-address.md) | `POST /AddressCapture/GetFullAddress.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/getfulladdress) |
| [Parse Name](actions/parse-name.md) | `POST /NameCleansing/ParseName.json` | [docs](https://docs.data-8.co.uk/web-services/namecleansing/parsename) |
| [Validate Bank Account](actions/validate-bank-account.md) | `POST /BankAccountValidation/IsValid.json` | [docs](https://docs.data-8.co.uk/web-services/bankaccountvalidation/isvalid) |
| [Validate Email Address](actions/validate-email-address.md) | `POST /EmailValidation/IsValid.json` | [docs](https://docs.data-8.co.uk/web-services/emailvalidation/isvalid) |
| [Validate IBAN](actions/validate-iban.md) | `POST /BankAccountValidation/IBANIsValid.json` | [docs](https://docs.data-8.co.uk/web-services/bankaccountvalidation/ibanisvalid) |
| [Validate Phone Number](actions/validate-phone-number.md) | `POST /PhoneValidation/IsValid.json` | [docs](https://docs.data-8.co.uk/web-services/phonevalidation/isvalid) |
| [Validate Postcode](actions/validate-postcode.md) | `POST /AddressCapture/ValidatePostcode.json` | [docs](https://docs.data-8.co.uk/web-services/addresscapture/validatepostcode) |
