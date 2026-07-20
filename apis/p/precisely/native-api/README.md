# Precisely: Native API Reference

A consolidated summary of Precisely's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/index.html
- **API base URL:** `https://api.precisely.com`

## Authentication

### API Key + Secret

Use your Precisely API key and API secret. MindCloud exchanges them for a bearer token automatically.

### Credentials

- **API Key:** `clientId` · required · Your Precisely API key.
- **API Secret:** `clientSecret` · required · Your Precisely API secret.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.precisely.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/GettingStarted/generating_an_oauth_token.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `location`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Geocode Address (Basic)](actions/geocode-address-basic.md) | `GET /geocode/v1/basic/geocode` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/Geocode/LI_Geo_GET_desc.html) |
| [Get PreciselyID By Address](actions/get-preciselyid-by-address.md) | `GET /geocode/v1/key/byaddress` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/PreciselyID/byPreciselyID/bypreciselyID.html) |
| [Key Lookup](actions/key-lookup.md) | `GET /geocode/v1/keylookup` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/key_lookup_get_request.html) |
| [Location By IP Address](actions/location-by-ip-address.md) | `GET /geolocation/v1/location/byipaddress` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geolocation/location_by_ip_address.html) |
| [Nearby Schools By Address](actions/nearby-schools-by-address.md) | `GET /schools/v1/school/byaddress` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Schools/School_ByAddress/school_byaddress.html) |
| [Nearest Intersection By Location](actions/nearest-intersection-by-location.md) | `GET /streets/v1/intersection/bylocation` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Streets/ByLocation/major_intersections_by_location.html) |
| [Nearest Speed Limit](actions/nearest-speed-limit.md) | `GET /streets/v1/speedlimit` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Streets/nearest_speed_limit/nearest_speed_limit.html) |
| [Reverse Geocode (Basic)](actions/reverse-geocode-basic.md) | `GET /geocode/v1/basic/reverseGeocode` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/ReverseGeocode/LI_revGeo_GET_desc.html) |
| [Timezone By Address](actions/timezone-by-address.md) | `GET /timezone/v1/timezone/byaddress` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/TimeZone/Timezone_address/timezone_by_address_get_request.html) |
| [Timezone By Location](actions/timezone-by-location.md) | `GET /timezone/v1/timezone/bylocation` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/TimeZone/Timezone_location/timezone_by_location_get_request.html) |
| [Typeahead Locations](actions/typeahead-locations.md) | `GET /typeahead/v1/locations` | [docs](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/AddressAutocomplete/addressautocomplete_desc.html) |
