# Smarty-streets: Native API Reference

A consolidated summary of Smarty-streets's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://www.smarty.com/docs
- **API base URL:** `https://us-street.api.smarty.com`

## Authentication

### Smarty Secret Key

Authenticate with a Smarty secret key pair.

### Credentials

- **Auth ID:** `username` · required
- **Auth Token:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.smarty.com/docs/account/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk ZIP Code Lookups](actions/bulk-zip-code-lookups.md) | `POST https://us-zipcode.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-zipcode-api/reference) |
| [Extract US Addresses Aggressively](actions/extract-us-addresses-aggressively.md) | `POST https://us-extract.api.smarty.com/` | [docs](https://www.smarty.com/docs/apis/us-extract-api/reference) |
| [Extract US Addresses From Text](actions/extract-us-addresses-from-text.md) | `POST https://us-extract.api.smarty.com/` | [docs](https://www.smarty.com/docs/apis/us-extract-api/reference) |
| [Get Property Data By SmartyKey](actions/get-property-data-by-smarty-key.md) | `GET https://us-enrichment.api.smarty.com/lookup/{smartyKey}/property` | [docs](https://www.smarty.com/docs/apis/us-enrichment-api/reference) |
| [Lookup International Postal Code](actions/lookup-international-postal-code.md) | `GET https://international-postal-code.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/international-postal-code-api/reference) |
| [Lookup ZIP Code Details](actions/lookup-zip-code-details.md) | `GET https://us-zipcode.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-zipcode-api/reference) |
| [Lookup ZIP Codes By City State](actions/lookup-zip-codes-by-city-state.md) | `GET https://us-zipcode.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-zipcode-api/reference) |
| [Reverse Geocode US Coordinates](actions/reverse-geocode-us-coordinates.md) | `GET https://us-reverse-geo.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-reverse-geocoding-api/reference) |
| [Reverse Geocode US Coordinates Including Non Postal Sources](actions/reverse-geocode-us-coordinates-including-non-postal-sources.md) | `GET https://us-reverse-geo.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-reverse-geocoding-api/reference) |
| [Suggest International Addresses](actions/suggest-international-addresses.md) | `GET https://international-autocomplete.api.smarty.com/v2/lookup` | [docs](https://www.smarty.com/docs/apis/international-autocomplete-api/reference) |
| [Suggest US Addresses](actions/suggest-us-addresses.md) | `GET https://us-autocomplete-pro.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-autocomplete-pro-api/reference) |
| [Validate City State ZIP Combination](actions/validate-city-state-zip-combination.md) | `GET https://us-zipcode.api.smarty.com/lookup` | [docs](https://www.smarty.com/docs/apis/us-zipcode-api/reference) |
| [Validate US Address And Return Invalid Detail](actions/validate-us-address-and-return-invalid-detail.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Address With Component Analysis](actions/validate-us-address-with-component-analysis.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Address With Enhanced Matching](actions/validate-us-address-with-enhanced-matching.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Address With IANA Timezone](actions/validate-us-address-with-iana-timezone.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Address With Project USA Format](actions/validate-us-address-with-project-usa-format.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Addresses In Bulk](actions/validate-us-addresses-in-bulk.md) | `POST https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Freeform Address](actions/validate-us-freeform-address.md) | `GET https://us-street.api.smarty.com/street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Validate US Street Address](actions/validate-us-street-address.md) | `GET /street-address` | [docs](https://www.smarty.com/docs/apis/us-street-api/reference) |
| [Verify International Address](actions/verify-international-address.md) | `GET https://international-street.api.smarty.com/verify` | [docs](https://www.smarty.com/docs/apis/international-street-api/reference) |
