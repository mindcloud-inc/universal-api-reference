# Namsor: Native API Reference

A consolidated summary of Namsor's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://namsor.app/api-documentation/introduction/
- **API base URL:** `https://v2.namsor.com/NamSorAPIv2`

## Authentication

### API Key

Authenticate requests to Namsor using the API key sent in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://namsor.app/api-documentation/introduction/)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Api Status](actions/api-status.md) | `GET /api2/json/apiStatus` | [docs](https://namsor.app/api-documentation/admin/) |
| [Api Usage](actions/api-usage.md) | `GET /api2/json/apiUsage` | [docs](https://namsor.app/api-documentation/admin/) |
| [Available Services](actions/available-services.md) | `GET /api2/json/apiServices` | [docs](https://namsor.app/api-documentation/admin/) |
| [Format Phone Number Geo](actions/format-phone-number-geo.md) | `GET /api2/json/phoneCodeGeo/:firstName/:lastName/:phoneNumber/:countryIso2` | [docs](https://namsor.app/api-documentation/phone-number-format/) |
| [Full Name Country](actions/full-name-country.md) | `GET /api2/json/country/:personalNameFull` | [docs](https://namsor.app/api-documentation/country-of-residence/) |
| [Full Name Country Batch](actions/full-name-country-batch.md) | `POST /api2/json/countryBatch` | [docs](https://namsor.app/api-documentation/country-of-residence/) |
| [Genderize Full Name](actions/genderize-full-name.md) | `GET /api2/json/genderFull/:fullName` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Full Name Batch](actions/genderize-full-name-batch.md) | `POST /api2/json/genderFullBatch` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Full Name Geo](actions/genderize-full-name-geo.md) | `GET /api2/json/genderFullGeo/:fullName/:countryIso2` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Full Name Geo Batch](actions/genderize-full-name-geo-batch.md) | `POST /api2/json/genderFullGeoBatch` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Name](actions/genderize-name.md) | `GET /api2/json/gender/:firstName/:lastName` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Name Batch](actions/genderize-name-batch.md) | `POST /api2/json/genderBatch` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Name Geo](actions/genderize-name-geo.md) | `GET /api2/json/genderGeo/:firstName/:lastName/:countryIso2` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Genderize Name Geo Batch](actions/genderize-name-geo-batch.md) | `POST /api2/json/genderGeoBatch` | [docs](https://namsor.app/api-documentation/gender-api/) |
| [Name Diaspora](actions/name-diaspora.md) | `GET /api2/json/diaspora/:countryIso2/:firstName/:lastName` | [docs](https://namsor.app/api-documentation/ethnicity/) |
| [Name Diaspora Batch](actions/name-diaspora-batch.md) | `POST /api2/json/diasporaBatch` | [docs](https://namsor.app/api-documentation/ethnicity/) |
| [Name Origin](actions/name-origin.md) | `GET /api2/json/origin/:firstName/:lastName` | [docs](https://namsor.app/api-documentation/origin/) |
| [Name Origin Batch](actions/name-origin-batch.md) | `POST /api2/json/originBatch` | [docs](https://namsor.app/api-documentation/origin/) |
| [Name US Race Ethnicity](actions/name-us-race-ethnicity.md) | `GET /api2/json/usRaceEthnicity/:firstName/:lastName` | [docs](https://namsor.app/api-documentation/us-race-ethnicity/) |
| [Name US Race Ethnicity Batch](actions/name-us-race-ethnicity-batch.md) | `POST /api2/json/usRaceEthnicityBatch` | [docs](https://namsor.app/api-documentation/us-race-ethnicity/) |
| [Name US Race Ethnicity ZIP5](actions/name-us-race-ethnicity-zip5.md) | `GET /api2/json/usRaceEthnicityZIP5/:firstName/:lastName/:zip5Code` | [docs](https://namsor.app/api-documentation/us-race-ethnicity/) |
| [Software Version](actions/software-version.md) | `GET /api2/json/softwareVersion` | [docs](https://namsor.app/api-documentation/admin/) |
| [Split Name](actions/split-name.md) | `GET /api2/json/parseName/:nameFull` | [docs](https://namsor.app/api-documentation/split-full-name/) |
| [Split Name Batch](actions/split-name-batch.md) | `POST /api2/json/parseNameBatch` | [docs](https://namsor.app/api-documentation/split-full-name/) |
